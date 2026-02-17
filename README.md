<div align="center">

# 💰 Agente Financeiro 💰
### App de Finanças Pessoais com Vibe Coding (Copilot + Lovable)

[![DIO](https://img.shields.io/badge/DIO-Bootcamp%20CAIXA-blueviolet)](https://www.dio.me/bootcamp/caixa-inteligencia-artificial-na-pratica)
![Status](https://img.shields.io/badge/status-MVP-success)
![Made with AI](https://img.shields.io/badge/made%20with-IA%20%F0%9F%A4%96-blue)

> Um app de finanças pessoais baseado em conversa: registre gastos/receitas, crie metas, veja relatórios e receba alertas — com mínima entrada manual.

</div>

---

## 🔗 Demo (resultado final)
- **Aplicação online:** https://simple-spent-chat.lovable.app

- **Print de tela:** https://github.com/user-attachments/assets/6fd9ccca-cf04-4da9-9a1d-2186e3bebd5d</a>

---

## 📌 Resumo do app (o que ele faz)
O **Agente Financeiro** é um app de finanças pessoais baseado em conversa que permite **registrar gastos e receitas em linguagem natural**, consultar **resumos do mês**, criar e acompanhar **metas**, visualizar **transações e relatórios**, além de receber **alertas financeiros**. A experiência é focada em reduzir esforço do usuário com **atalhos de ação**, confirmação rápida e, no MVP, pode incluir **importação opcional de transações via SMS/notificações**, **categorização automática** e **recomendações educativas**.

---

## ✨ Funcionalidades (MVP)
- 💬 **Chat com IA** para registrar despesas e receitas (linguagem natural)
- ⚡ **Atalhos rápidos**: registrar gasto, registrar receita, ver resumo, criar meta
- 🧾 **Histórico de transações** com visualização e organização
- 🎯 **Metas financeiras** por categoria e acompanhamento de progresso
- 📊 **Relatórios** simples (por período/categoria)
- 🔔 **Alertas** (vencimentos e variações de consumo)
- 🔐 **Privacidade**: exportar dados e excluir conta/dados
- 📩 *(Opcional no MVP)* **Importação automática** via SMS/notificações com revisão (Confirmar/Editar/Ignorar)

---

## 🧠 Prompt final (PRD) — entregue para a IA (Copilot/Lovable)
> Abaixo está o **prompt final** usado como PRD refinado para construir o app.

```markdown
Você é um Product Builder. Crie um aplicativo móvel de Finanças Pessoais orientado por conversa (chat) com importação opcional de transações via SMS/notificações.
NOME DO APP
- Nome: Agente Financeiro
OBJETIVO
- Permitir que usuários iniciantes registrem, acompanhem e monitorem finanças pessoais com mínima entrada manual.
- Entrada: (1) chat em linguagem natural (texto e áudio->texto), (2) importação automática de transações a partir de SMS/notificações de bancos (quando permitido).
- Saídas: relatórios simples, metas, alertas de vencimento e alertas de variação de consumo por categoria, e dicas do “Agente Financeiro”.
PLATAFORMA
- Prioridade: Android 
MOEDA E LOCAL
- Moeda padrão: BRL
- Idioma: pt-BR
CATEGORIAS PADRÃO (MVP)
- Categorias: Alimentação, Transporte, Moradia, Saúde, Lazer, Educação, Contas, Assinaturas, Transferências, Investimentos, Outros
    - Usuário deve poder criar, excluir, consultar e alterar categorias
ESCOPO (MVP)
MUST:
1) Onboarding com consentimentos e permissões (SMS/notificação opcional).
2) Tela principal de Chat para registrar transações.
3) Extração de campos: tipo (gasto/receita), valor, data, descrição/merchant.
4) Classificação automática em categorias e possibilidade de correção em 1 toque.
5) Tela “Revisar importações” com Confirmar/Editar/Ignorar.
6) Metas simples por categoria (limite mensal) e progresso.
7) Alertas: vencimento de contas recorrentes e aumento/diminuição relevante por categoria.
8) Relatórios simples: gastos por categoria e total por período.
9) Configurações de privacidade: exportar dados e excluir dados/conta.
REGRAS DE CONVERSA
- Seja claro sobre o que o app consegue fazer e ofereça sugestões rápidas.
- Ao registrar transação: se faltar valor ou tipo, faça só 1 pergunta objetiva por vez.
- Sempre confirme em 1 linha antes de salvar e ofereça “Editar”.
- Se não entender: mostre 3 opções (Registrar gasto | Ver resumo | Criar meta).
MODELO DE DADOS
User(id, nome, moeda, consent_sms, consent_notif, preferencias_alerta)
Transaction(id, user_id, type, amount, date, merchant_text, category_id, source, confidence, status)
Category(id, name, parent_id)
Rule(id, user_id, pattern_type, pattern_value, category_id)
Goal(id, user_id, type, category_id, amount_target, period, start_date, active)
RecurringBill(id, user_id, name, due_day, expected_amount, category_id, remind_days_before)
Alert(id, user_id, kind, message, created_at, clicked_at)
TELAS
1) Onboarding
2) Home/Chat
3) Revisar Importações
4) Transações
5) Detalhe Transação
6) Metas
7) Relatórios/Insights
8) Alertas & Contas
9) Configurações
VALIDAÇÃO
- Eventos: transacao_criada, importacao_confirmada, importacao_ignorada, meta_criada, alerta_clicado.
- Feedback de dicas: (útil/não útil).
ENTREGA
- Gere estrutura do app, modelo de dados, telas e fluxos.
- Tom educativo e português do Brasil.
