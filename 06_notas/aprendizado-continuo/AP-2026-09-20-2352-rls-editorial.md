# AP-2026-09-20-2352 — RLS editorial deve carregar invariantes de transição

- **Status**: promovido
- **Escopo**: projeto do cliente
- **Task/SPEC**: F1-T02 / SPEC-1-001
- **Sinal**: a primeira prova permitiu aprovação sem fonte porque o hook de ciclo de vida não estava efetivamente carregado; a correção foi tornar a regra de aprovação/publicação explícita no RLS, com `source_count > 0`, e manter o rascunho sem fonte permitido para testar a recusa posterior.
- **Evidência**: migrations `0005`, `0006` e `0007` aplicadas no SkipCloud; schema efetivo confirmou `source_count` e regras de update; bateria final passou criação de DRAFT, recusa de publicação por operator, revisão/aprovação/publicação/arquivamento, recusa de aprovação sem fonte, bloqueio de autoelevação e persistência do histórico.
- **Regra reutilizável**: invariantes de autorização e transição que protegem publicação devem existir no RLS efetivo da collection, não somente na interface ou em hooks; rascunhos incompletos devem ser permitidos para revisão, mas toda transição para `APPROVED`/`PUBLISHED` precisa exigir fonte, revisor e alçada correta. Após qualquer migration, inspecionar o schema vivo e repetir uma prova negativa.
- **Quando aplicar**: toda área editorial ou workflow com estados, papéis e publicação controlada em SkipCloud/PocketBase.
- **Quando não aplicar**: coleções sem transição editorial ou sem controle de publicação.
- **Confiança**: alta — regra confirmada por falha reproduzida, correção aditiva, schema vivo e bateria final aprovada.
- **Privacidade**: sem segredo, dado pessoal ou conteúdo jurídico real; somente metadados e fixtures sintéticas.
