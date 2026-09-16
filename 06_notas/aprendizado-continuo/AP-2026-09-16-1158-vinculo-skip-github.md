# AP-2026-09-16-1158 — Vínculo Skip↔GitHub e sincronização operacional

- Status: candidato
- Escopo: projeto do cliente
- Task/SPEC: F1-T01 / SPEC-1-001
- Sinal: o projeto Skip confirma o projeto Agrojur e o preview, mas não expõe na API a relação formal com o repositório; a API GitHub permite leitura e retorna 404 nas tentativas observáveis de escrita.
- Evidência: Skip projectId 58949, preview v0.0.2 (`274b57e`), `mcp_github_get_file_contents` com leitura bem-sucedida e tentativas de atualização retornando 404.
- Regra reutilizável: antes de fechar uma task que exige vínculo documental, validar separadamente a existência do ambiente, a relação ambiente↔repositório e a capacidade de sincronizar os registros canônicos.
- Quando aplicar: em todo fechamento de task do Adapta que dependa de recibo de projeto, vínculo externo ou escrita em repositório.
- Quando não aplicar: quando o critério não exigir vínculo externo nem atualização de registros canônicos.
- Confiança: alta — observação repetida em leitura e escrita das APIs durante a mesma task.
- Privacidade: sem segredo, dado pessoal ou conteúdo bruto.
