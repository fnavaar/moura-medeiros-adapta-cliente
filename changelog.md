# Changelog

## 2026-09-22
- 2026-09-22 · Celso · Task F1-T03 concluída: regressão de segurança e rollback editorial aprovados no preview `https://agrojur-436c9--preview.goskip.app`.
- Evidências técnicas: Skip v0.0.11 (`644a0c7`), migration `0008_secure_history_recovery` aplicada, histórico restrito, rota autenticada, recuperação `ARCHIVED→IN_REVIEW`, nova aprovação antes de republicar, provas 401/403, autoelevação, slug/fonte/transição, scan e logs sanitizados.
- Aceite humano: Celso entrou na Área editorial com a fixture sintética e confirmou em 22/09/2026: “Entrei e funcionou”. Produção permaneceu não publicada e não houve uso de conteúdo real.
- Aprendizado promovido: o handoff de teste deve entregar explicitamente URL, usuário e senha sintéticos e resultado esperado; o cliente não deve precisar adivinhar credenciais. A senha não foi registrada no aprendizado.

## 2026-09-20
- 2026-09-20 · Celso · Task F1-T02 concluída: área editorial protegida com estados `DRAFT`, `IN_REVIEW`, `APPROVED`, `PUBLISHED` e `ARCHIVED`, autenticação, papéis separados, histórico persistente e recusa server-side de publicação incompleta ou indevida.
- Evidências técnicas: Skip v0.0.10 (`83e9d05`), migrations `0001`–`0007` aplicadas, collections `contents` e `content_versions`, QA oficial integral e bateria final de RBAC, transições, histórico, fonte obrigatória e rollback por arquivamento.
- Aceite humano: Celso testou o preview `https://agrojur-436c9--preview.goskip.app` e confirmou que a F1-T02 funcionou em 20/09/2026.
- Produção permaneceu não publicada; foram preservadas apenas fixtures sintéticas e o noindex do preview.
- F1-T03 ficou liberada para futura análise, sem autorização presumida para implementação.

## 2026-09-16
- 2026-09-16 · Celso · Task F1-T01 concluída: projeto Skip Agrojur 58949, preview público noindex, repositório `cbmadvmoura-cell/agrojur-9d0q1w5lj` e commits do Skip confirmados; QA oficial, cinco rotas e teste humano aprovados.
- Evidência complementar: o repositório gerado pelo Skip contém `Initial sync: Agrojur` e o commit `42173df7a995a6195b3bb56b53418adc809e0498` da implementação do shell.
- Checkpoint anterior: a implementação havia sido aprovada, mas CA-1-001 ainda estava pendente naquele momento; o bloqueio foi resolvido após a confirmação do repositório gerado pelo Skip no GitHub.
- Sincronização dos registros canônicos observada no commit `21eaba06818138a90de5e59ab9b5b4644d45b76c` do repositório operacional. As tentativas iniciais de escrita que retornaram `404 Not Found` foram superadas pela gravação posterior aceita no branch `main`.

## 2026-09-14
- Workspace externo criado com o recorte da Fase 1. Nenhuma task ou integração executada.

- 2026-09-22 · Ethos · F1-T04 em teste humano: pacote B1-CONT-01 v0.1.0-draft preparado em `04-fase-atual/b1-cont-01/` com inventário do acervo disponível, copy de home, manifesto não importável, matriz de fontes/autoria/revisão, checklist de publicidade/PII e recibo da metodologia da Fase 2.
- Verificações automatizáveis passaram: JSON/índice, `git diff --check`, triagem de PII/segredos e políticas. O pacote permanece DRAFT/BLOCKED; conteúdo real não foi criado/importado/publicado; aceite de Celso pendente.
- 2026-09-26 · Celso aprovou apenas parte da copy de home como rascunho (título, subtítulo e aviso informativo); o registro foi feito em `02-copy-home-draft.md` e o restante do B1-CONT-01 permanece DRAFT/BLOCKED. Próxima revisão proposta: foco/intenção do cluster de crédito rural, distinguindo a prorrogação da operação existente de linha nova de composição; sem autorização de publicação ou importação.
- 2026-09-26 · Celso escolheu manter o foco preliminar de crédito rural apenas como direção do rascunho (questionar, quando houver fundamento no caso concreto, a recusa em prorrogar operação já contratada; linha nova de composição separada). Decisão anotada no manifesto draft, matriz e índice B1-CONT-01; pacote continua DRAFT/BLOCKED, sem aprovação final, importação ou publicação.
