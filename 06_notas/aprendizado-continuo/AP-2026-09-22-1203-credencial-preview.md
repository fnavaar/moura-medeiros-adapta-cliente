# AP-2026-09-22-1203 — Handoff de credencial sintética no teste humano

- **Status**: promovido
- **Escopo**: projeto do cliente
- **Task/SPEC**: F1-T03 / SPEC-1-001
- **Sinal**: o cliente validou o preview, mas inicialmente não conseguiu entrar na Área editorial porque o roteiro não entregava explicitamente a credencial sintética; a tela pré-preenchia a conta, porém a senha não havia sido informada.
- **Evidência**: inspeção read-only confirmou a fixture de autenticação no código/ambiente; a entrada no preview foi validada com a credencial sintética e o cliente confirmou “Entrei e funcionou”. Nenhum dado real, segredo de produção ou conteúdo jurídico foi usado.
- **Regra reutilizável**: todo handoff de teste humano de área autenticada deve informar explicitamente URL do ambiente, usuário sintético, senha sintética, escopo seguro, resultado esperado e condição de parada. O cliente nunca deve precisar adivinhar uma credencial; a senha não deve ser repetida em aprendizados, changelog ou memória permanente.
- **Quando aplicar**: qualquer preview autenticado, fixture de RBAC ou teste manual que dependa de conta sintética.
- **Quando não aplicar**: acesso de produção ou credenciais reais, que devem seguir o procedimento próprio de segurança e nunca ser compartilhados em chat.
- **Confiança**: alta — bloqueio observado no teste humano, causa confirmada por inspeção do código e sucesso reproduzido no preview.
- **Privacidade**: sem senha armazenada; apenas regra operacional e metadados do ambiente.
