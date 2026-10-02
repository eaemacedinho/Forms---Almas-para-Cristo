# Luau — Almas para Cristo

Aplicação mobile-first para inscrições do Luau Católico (23/10, 22h até o Rosário das 04h).

## Escopo aprovado
- 100 vagas, com lista de espera e reservas temporárias atômicas.
- Inscrição individual, inclusive menores com autorização verificável do responsável.
- Convite digital personalizado compartilhável, sem dados pessoais expostos.
- Alimentação organizada pela equipe (sem lanche partilhado obrigatório).
- Ingressos pagos, valor final ainda pendente (R$10 ou R$20); cortesias geridas pela coordenação.
- Status separados: iniciado, aguardando pagamento, aguardando autorização, confirmado, cancelado e lista de espera.
- Nunca confirmar ingresso antes de confirmação confiável do pagamento e autorização quando necessária.

## Stack proposta
React, TypeScript, Tailwind, Framer Motion, Firebase Hosting, Firestore, Auth e backend confiável para pagamentos/webhooks, reservas e promoções de lista de espera. Firebase project: luau---almas-para-cristo. Nunca versionar segredos ou credenciais.

## Telas
1. Apresentação do evento
2. Identificação e acolhimento
3. Alimentação e acessibilidade (campos opcionais e privados)
4. Autorização de responsável, quando aplicável
5. Revisão e pagamento
6. Confirmação e convite digital
7. Painel administrativo protegido

## Decisões pendentes
- Preço definitivo, orçamento e política de reembolso.
- Provedor de pagamento e conta recebedora.
- Prazo de reserva e autorização de menores, texto aprovado pela paróquia.
- Política de privacidade e consentimento separado para uso de imagem.

## Segurança
Regras Firestore de mínimo privilégio; transações no servidor; idempotência de webhook; controle de concorrência; nenhuma lista de inscritos pública; testes de capacidade, cancelamento e lista de espera.
