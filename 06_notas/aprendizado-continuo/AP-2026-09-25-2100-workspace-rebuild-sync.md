# AP-2026-09-25-2100 — Rebuild do workspace apaga plugins/ e repos/; sincronizar ao fim de cada ciclo

- **Status**: promovido
- **Escopo**: projeto do cliente
- **Task/SPEC**: F1-T04 / SPEC-1-002 (observado durante retomada operacional em 25/09/2026)
- **Sinal**: o rebuild do workspace ETHOS (imagem baked) apaga diretórios fora da imagem — `plugins/` e `repos/` — quebrando os symlinks de `skills/{skill-mind-cliente,proxima-task,executar-task,debug-task,concluir-task,status,aprendizado-continuo}` e o clone do repositório operacional. Segunda ocorrência (22/09 e 25/09). Na retomada de 25/09, os registros canônicos da F1-T02/T03 e o pacote B1-CONT-01 estavam há 3 dias apenas no workspace local, sem commit/push.
- **Evidência**: `ls -la skills/` exibiu symlinks para caminhos inexistentes; `plugins/` ausente; `git status` do clone refeito mostrou 6 arquivos modificados e 3 não rastreados pendentes desde 22/09. Restauração reproduzível: clonar `https://github.com/drkgod/Plugin-Cliente---Adapta`, fixar no commit `36154ba2406a251a930171ad50c3a3bf3dd93493` (v0.3.0) em `plugins/Plugin-Cliente---Adapta/adapta-cliente/` e re-clonar `https://github.com/fnavaar/moura-medeiros-adapta-cliente` em `repos/`. Sincronização do checkpoint executada em 25/09 e confirmada pelo commit remoto `66d823e97c68d4b864402c192e95997d665cf963`.
- **Regra reutilizável**: ao fim de cada ciclo de execução/debug, commitar e sincronizar o repositório operacional antes de encerrar — trabalho não sincronizado pode se perder num rebuild. Após qualquer rebuild, restaurar o plugin pelo commit fixado v0.3.0, re-clonar o repo operacional em `repos/` e reconciliar com `origin/main` antes de qualquer escrita.
- **Quando aplicar**: toda sessão que trabalhe no repositório operacional do cliente neste runtime; toda retomada após rebuild.
- **Quando não aplicar**: alterações que dependam de gate humano pendente — o checkpoint preserva o trabalho, mas não muda gates nem aprova nada.
- **Confiança**: alta — falha reproduzida duas vezes, restauração verificada e sincronização confirmada por SHA remoto observável.
- **Privacidade**: sem segredo, credencial, dado pessoal ou conteúdo jurídico real; apenas caminhos, hashes e procedimento.
