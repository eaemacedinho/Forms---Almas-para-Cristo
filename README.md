# Luau — Almas para Cristo

Formulário mobile-first para o Luau Católico, previsto para 23/10 às 22h até o Rosário das 04h.

## Definições
- 100 vagas com lista de espera; menores com autorização verificável dos responsáveis.
- Convite digital personalizado, compartilhável sem divulgar dados pessoais.
- Alimentação organizada pela equipe e custeada pelos ingressos; não há lanche partilhado obrigatório.
- Ingressos pagos via Pix; preço oficial ainda pendente (considerando R$10/R$20; R$15 apenas simulação).
- Recebimento: conta PagSeguro/PagBank em nome de Murilo, reitor do grupo e responsável pela conta; divulgar corretamente a titularidade ao pagador.
- Registrar consentimento do titular e combinar prestação de contas, reembolsos e eventual tratamento fiscal com ele.
- Cortesias autorizadas pela coordenação.

## Fluxo
1. Apresentar informações e preço; coletar somente dados necessários.
2. Reservar vaga temporária via transação atômica no backend.
3. Criar cobrança Pix com integração oficial do PagBank, condicionada à habilitação e elegibilidade da conta do titular.
4. Confirmar somente após consulta confiável e/ou notificação autenticada do provedor; usar idempotência.
5. Para menores, emitir ingresso somente após pagamento e autorização verificável do responsável.
6. Expirar reservas não pagas, promover lista de espera e tratar pagamentos atrasados sem ultrapassar 100 vagas.
7. Gerar convite digital e oferecer confirmação e consulta do status sem expor dados.

## Tecnologia
React, TypeScript, Tailwind, Framer Motion, Firebase Hosting, Firestore, Auth para coordenadores, backend seguro (Cloud Functions ou equivalente). Firebase project informado: `luau---almas-para-cristo`. Credenciais do PagBank e Firebase ficam exclusivamente em ambiente seguro; nunca no repositório ou frontend.

## Telas
Boas-vindas; identificação e acolhimento; alimentação/acessibilidade; autorização de menor (quando aplicável); revisão e Pix; convite digital; painel protegido.

## Pendências antes de ativar pagamentos
- Confirmar acesso do titular Murilo a integrações/API e credenciais de produção do PagBank, sem compartilhar tokens em chat ou GitHub.
- Definir preço, orçamento, política de cancelamento/reembolso e prazo de reserva.
- Aprovar texto de autorização dos responsáveis, privacidade e consentimento separado de imagem.
- Testar sandbox, notificações, pagamento duplicado/tardio, expiração e limite de 100 vagas.

## Segurança
Transações no servidor, regras Firestore restritivas, autenticação do painel, validação de notificações, idempotência e tratamento privado dos dados de participantes.
