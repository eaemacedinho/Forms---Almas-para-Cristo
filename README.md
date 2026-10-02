# Luau — Almas para Cristo

Formulário mobile-first de inscrições para o Luau Católico, 23/10, às 22h, terminando no Rosário das 04h.

## Definições aprovadas
- Capacidade: 100 vagas, com lista de espera.
- Menores podem participar com autorização verificável de seus responsáveis.
- Convite digital personalizado compartilhável sem exposição de dados pessoais.
- Alimentação será organizada pela equipe, custeada pelos ingressos, sem lanche partilhado obrigatório.
- Ingressos pagos via Pix; **recebedor: conta do Almas para Cristo**.
- Preço final pendente (avaliando R$10, R$15 ou R$20). Não cobrar até a definição.
- Cortesias para participantes autorizadas pela coordenação.

## Fluxo de pagamento e capacidade
1. Coletar dados mínimos e informar preço antes da finalização.
2. Reservar vaga temporariamente por transação atômica no backend.
3. Criar cobrança Pix por provedor compatível com a titularidade da conta do Almas para Cristo.
4. Validar webhook autenticado e idempotente e conciliar pagamento antes de confirmar.
5. Para menores, só liberar ingresso após autorização verificável do responsável, além do pagamento.
6. Expirar reservas não pagas e oferecer vagas à lista de espera em ordem definida.
7. Definir procedimento de reembolso para pagamentos tardios após expiração da reserva, evitando overselling.

## Stack proposta
React, TypeScript, Tailwind, Framer Motion, Firebase Hosting, Firestore, Authentication para administradores e backend confiável (Cloud Functions ou equivalente) para pagamentos e capacidade. Firebase project ID informado: `luau---almas-para-cristo`. Nunca versionar credenciais, chaves Pix privadas ou tokens.

## Telas
1. Boas-vindas e apresentação
2. Identificação e acolhimento
3. Alimentação e acessibilidade (dados opcionais e restritos)
4. Autorização do responsável quando aplicável
5. Revisão e pagamento Pix
6. Ingresso personalizado e compartilhamento
7. Painel administrativo protegido: vendas, capacidade, pendências e lista de espera

## Decisões pendentes
- Titularidade formal e provedor compatível com a conta recebedora; configuração segura de credenciais.
- Preço oficial, orçamento e política de reembolso.
- Prazo de reserva, prazo para autorização de menores e regras aprovadas pela paróquia.
- Política de privacidade, consentimento separado para uso de imagem e regras de retenção de dados.

## Segurança
Firestore com mínimo privilégio; transações no servidor; webhooks autenticados e idempotentes; controle de concorrência; dados dos inscritos privados; testes de limite, cancelamento, lista de espera e pagamentos atrasados.
