# 🎮 Xbox Game Pass — Sales Dashboard

Dashboard de vendas do serviço de assinatura XBOX GAMEPASS

---

## 📌 Sobre o projeto

O dashboard analisa uma base de **assinaturas do Xbox Game Pass Ultimate**, cobrindo o período de **01/01/2024 a 31/12/2024**, e responde a perguntas de negócio como:

1. Qual é o faturamento total de vendas de planos anuais, considerando todas as assinaturas agregadas?
2. Qual é o faturamento total de planos anuais, separado por com e sem autorenovação?
3. Qual o total de vendas do add-on **EA Play Season Pass**?
4. Qual o total de vendas do add-on **Minecraft Season Pass**?
5. Quanto do faturamento foi vendido com e sem desconto (cupom)?
6. Quanto cada componente (assinatura base, EA Play, Minecraft) representa da receita total?

Todo o tratamento é feito nativamente em Excel, sem ferramentas externas: os dados brutos ficam intactos em uma aba própria, e todos os KPIs e gráficos do painel são alimentados por **Tabelas Dinâmicas** e fórmulas que recalculam automaticamente.

---

## 🗂️ Estrutura do arquivo

O workbook é organizado em 4 abas:

| Aba | Conteúdo |
|---|---|
| **Dashboard** | Painel executivo: KPIs de faturamento, composição da receita por produto e segmentação (slicer) por tipo de assinatura |
| **Base** | Dados brutos — uma linha por assinante, sem nenhuma alteração |
| **Calculos** | Tabelas Dinâmicas que respondem cada uma das 6 perguntas de negócio, usadas como fonte dos gráficos e KPIs do Dashboard |
| **Assets** | Paleta de cores e elementos visuais (logos/ícones) usados no design do painel |

### Colunas da base (`Base`)

| Coluna | Descrição |
|---|---|
| Subscriber ID | Identificador único do assinante |
| Name | Nome do assinante |
| Plan | Plano contratado (Ultimate) |
| Start Date | Data de início da assinatura |
| Auto Renewal | Se a assinatura tem autorenovação ativa (Yes/No) |
| Subscription Price | Valor da assinatura base |
| Subscription Type | Periodicidade (Monthly, Quarterly, Annual) |
| EA Play Season Pass | Se o assinante contratou o add-on EA Play (Yes/No) |
| EA Play Season Pass Price | Valor do add-on EA Play |
| Minecraft Season Pass | Se o assinante contratou o add-on Minecraft (Yes/No) |
| Minecraft Season Pass Price | Valor do add-on Minecraft |
| Total Value Without Coupon | Valor total antes do desconto |
| Coupon Value | Valor do desconto aplicado |
| Total Value | Valor total líquido (após desconto) |

> A base é um conjunto de dados simulado, criado para fins do desafio.

---

## 🖱️ Como explorar o dashboard

1. Baixe e abra `Dashboard_Xbox.xlsx` no Excel (as Tabelas Dinâmicas e a Segmentação de Dados exigem o Excel desktop; o Excel Online pode não exibir todos os elementos corretamente)
2. Vá até a aba **Dashboard** para ver o resumo executivo
3. Use a **Segmentação de Dados (slicer)** de *Subscription Type* para filtrar o painel por periodicidade (Monthly, Quarterly, Annual)
4. Para entender o cálculo por trás de cada KPI, veja a aba **Calculos** — cada Tabela Dinâmica está logo abaixo da pergunta de negócio correspondente
5. A aba **Base** contém os dados brutos, caso queira auditar ou refazer alguma análise

---

## 🛠️ Como foi construído

- Microsoft Excel — sem scripts, macros ou ferramentas externas
- **Tabelas Dinâmicas (PivotTables)** para agregações por tipo de assinatura
- **Gráficos de barras** nativos do Excel conectados às Tabelas Dinâmicas
- **Segmentação de Dados (Slicer)** para filtro interativo por `Subscription Type`
- Paleta de cores e identidade visual próprias, documentadas na aba Assets

---
Paleta de cores e identidade visual próprias, documentadas na aba Assets
