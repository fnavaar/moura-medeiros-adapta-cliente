# B1-CONT-01 — Inventário, auditoria e contrato do primeiro cluster

- **Task:** F1-T04
- **SPEC:** `04_fase-atual/specs/spec-1-002.md`
- **Versão do pacote:** `0.1.0-draft`
- **Estado:** `DRAFT/BLOCKED`
- **Responsável pela decisão:** Celso
- **Data de preparação:** 2026-09-22
- **Regra de publicação:** nenhum item deste pacote pode ser importado ou publicado antes do aceite explícito de Celso e da conferência dos revisores temáticos.

## Objetivo

Preparar o contrato editorial mínimo para o primeiro cluster do Portal Agrojur, sem inventar tema, conteúdo jurídico, fonte, autoria ou aprovação que não estejam disponíveis. O pacote separa:

1. o que foi encontrado no acervo entregue;
2. o que é apenas fixture sintética já existente no preview;
3. o que ainda precisa de decisão humana;
4. o que não pode entrar no produto sem aprovação e revisão.

## Resultado da auditoria de entrada

A auditoria foi feita no repositório operacional `fnavaar/moura-medeiros-adapta-cliente` e, em leitura somente, no repositório do projeto Skip `cbmadvmoura-cell/agrojur-9d0q1w5lj`.

### Acervo disponível

- O repositório operacional contém documentos de visão, constituição, ata de corte, SPECs, registros de execução e documentos de setup; não contém compilado de artigos, pautas, fontes temáticas, autores ou revisores cadastrados.
- O repositório do projeto Skip contém o shell público e fixtures demonstrativas em `src/pages/Index.tsx` e `src/pages/PortalSection.tsx`; não foi encontrado manifesto editorial, cluster aprovado, coleção editorial ou conteúdo jurídico real.
- O schema PocketBase versionado no projeto Skip contém somente a coleção de autenticação `users` no snapshot auditado; não há contrato de conteúdo/cluster nesse snapshot.
- O arquivo `.env` do projeto Skip foi deliberadamente **não aberto**; nenhuma credencial ou segredo foi copiado para este pacote.

### Classificação do material encontrado

| ID | Material | Local/fonte | Classe | Decisão nesta task | Motivo |
|---|---|---|---|---|---|
| INV-001 | Visão: portal regional para produtores e empresas do agro em MT | `01_projeto/visao-do-projeto.md` | Governança | Manter como restrição de escopo | Não é conteúdo publicável nem fonte temática |
| INV-002 | Público, foco MT, conteúdo governado, sem PJe | `04_fase-atual/specs/spec-1-002.md` e ata de corte | Governança | Manter como restrição | Decisões fechadas da SPEC |
| INV-003 | Copy do shell do preview | repositório Skip, `src/pages/Index.tsx` | Fixture sintética | Não importar como conteúdo real | O próprio shell sinaliza ambiente de teste/conteúdo sintético |
| INV-004 | Cartões demonstrativos de Temas/Blog | repositório Skip, `src/pages/PortalSection.tsx` | Fixture sintética | Não importar como cluster | Não possuem manifesto, fonte, autor/revisor ou aprovação |
| INV-005 | Conteúdo jurídico do compilado estratégico | Acervo citado pela SPEC | Não localizado | Bloqueado | Nenhum arquivo foi entregue para auditoria |
| INV-006 | Fontes primárias por tema | Entradas previstas na SPEC | Não localizado | Bloqueado | Tema e itens ainda não aprovados |
| INV-007 | Autores e revisores temáticos | Entradas previstas na SPEC | Não localizado | Bloqueado | Equipe por tema ainda não nomeada |
| INV-008 | Dados pessoais do acervo | Risco indicado pela SPEC | Não localizado | Não migrar | Exige allowlist e decisão de tratamento; nenhum dado foi copiado |

## Conclusão da auditoria

O acervo efetivamente disponível não permite selar o primeiro cluster. O pacote técnico fica pronto para decisão, mas `B1-CONT-01` permanece **não aprovado** até Celso fornecer/aprovar o inventário temático, a copy da home, o manifesto, as fontes, autores/revisores e a solicitação da metodologia da Fase 2.

Nenhum conteúdo jurídico real foi criado, resumido, atribuído ou colocado em allowlist nesta task.
