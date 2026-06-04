# 🚀 PassoAPasso.md

# Criando uma Ferramenta de Controle de Investimentos com Excel

## 📖 Introdução

Este documento descreve todo o processo de construção da ferramenta de simulação de investimentos em Fundos Imobiliários (FIIs), desenvolvida como parte do desafio da DIO.

O objetivo é criar uma planilha capaz de auxiliar investidores na tomada de decisões financeiras através da projeção de patrimônio, dividendos e rentabilidade ao longo do tempo.

------

# 🎯 Objetivo da Solução

A ferramenta deverá permitir que o usuário:

- Informar o valor que pretende investir mensalmente.
- Definir o prazo do investimento.
- Escolher uma taxa de rendimento.
- Simular o crescimento do patrimônio.
- Calcular dividendos futuros.
- Comparar cenários de investimento.
- Obter uma visão clara do potencial retorno financeiro.

------

# 📋 Etapa 1 - Planejamento da Solução

Antes de abrir o Excel, é importante entender quais perguntas a planilha deverá responder.

### Perguntas de Negócio

- Quanto preciso investir por mês?
- Quanto terei acumulado em 5, 10, 20 ou 30 anos?
- Quanto receberei de dividendos?
- Qual o impacto de aumentar meus aportes?
- Qual cenário oferece melhor retorno?

Essas perguntas servirão como base para toda a construção da planilha.

------

# 📊 Etapa 2 - Criando a Área de Entrada de Dados

Crie uma seção destinada aos parâmetros informados pelo usuário.

## Campos sugeridos

| Campo                        | Exemplo  |
| ---------------------------- | -------- |
| Salário                      | R$ 5.000 |
| Percentual para Investimento | 20%      |
| Valor Inicial                | R$ 1.000 |
| Aporte Mensal                | R$ 500   |
| Prazo                        | 10 anos  |
| Taxa de Rendimento           | 0,8%     |

------

# 🧮 Etapa 3 - Criando as Variáveis Globais

Para facilitar a manutenção da planilha, utilize o recurso:

## Fórmulas → Gerenciador de Nomes

Criar nomes para os intervalos:

| Nome       |
| ---------- |
| salario    |
| aporte     |
| prazo      |
| taxa       |
| patrimonio |
| dividendos |

Isso tornará as fórmulas mais legíveis.

Exemplo:

```excel
=aporte*12
```

em vez de:

```excel
=B4*12
```

------

# 💰 Etapa 4 - Calculando o Valor Total Investido

Determinar quanto dinheiro foi efetivamente aplicado ao longo do período.

### Fórmula

```excel
=APORTE_MENSAL*(ANOS*12)
```

### Exemplo

Aporte:

R$ 500

Prazo:

10 anos

Resultado:

```text
500 x 120 = R$ 60.000
```

------

# 📈 Etapa 5 - Simulando o Patrimônio Acumulado

Nesta etapa aplicamos juros compostos.

O Excel disponibiliza a função:

```excel
=VF()
```

Exemplo:

```excel
=VF(TAXA;MESES;-APORTE;0;0)
```

Onde:

- VF = Valor Futuro
- TAXA = rendimento mensal
- MESES = prazo total
- APORTE = investimento mensal

Resultado esperado:

Patrimônio acumulado ao final do período.

------

# 🏢 Etapa 6 - Simulando Dividendos

Fundos Imobiliários distribuem rendimentos periodicamente.

Calcular:

```excel
=PATRIMONIO*DY
```

Onde:

DY = Dividend Yield

Exemplo:

Patrimônio:

R$ 500.000

DY:

0,8%

Resultado:

```text
R$ 4.000 por mês
```

------

# 📉 Etapa 7 - Criando Simulador de Cenários

Criar três cenários para comparação.

## Conservador

```text
0,6% ao mês
```

## Moderado

```text
0,8% ao mês
```

## Agressivo

```text
1,0% ao mês
```

A mesma entrada poderá gerar três projeções diferentes.

Isso ajuda o investidor a visualizar riscos e oportunidades.

------

# 📊 Etapa 8 - Construindo o Dashboard

Criar uma área visual com indicadores.

Sugestões:

### Indicadores

- Valor Investido
- Patrimônio Acumulado
- Rentabilidade
- Dividendos Mensais

### Gráficos

- Evolução Patrimonial
- Crescimento dos Dividendos
- Comparativo de Cenários

------

# 🎨 Etapa 9 - Melhorando a Experiência Visual

Aplicar padronização visual.

## Recomendações

### Cores

Verde:
Indicadores positivos

Vermelho:
Indicadores negativos

Azul:
Informações gerais

------

### Formatação

- Formato Moeda
- Percentual
- Bordas padronizadas
- Títulos destacados

------

# 🔍 Etapa 10 - Testando a Ferramenta

Validar diferentes cenários.

## Teste 1

Aporte:

R$ 100

Prazo:

5 anos

------

## Teste 2

Aporte:

R$ 500

Prazo:

15 anos

------

## Teste 3

Aporte:

R$ 1.000

Prazo:

30 anos

------

Verificar:

- Patrimônio
- Rentabilidade
- Dividendos

------

# 📂 Etapa 11 - Documentando o Projeto

Criar um README.md contendo:

## Sobre o Projeto

Objetivo da ferramenta.

## Funcionalidades

- Simulação de patrimônio
- Simulação de dividendos
- Comparação de cenários

## Tecnologias

- Microsoft Excel
- Fórmulas Financeiras
- Dashboard

## Capturas de Tela

Adicionar imagens da planilha.

------

# ☁️ Etapa 12 - Publicando no GitHub

Criar um repositório público.

Exemplo:

```text
controle-investimentos-excel
```

Enviar:

- README.md
- PassoAPasso.md
- Planilha Excel
- Imagens

------

# 🏆 Resultado Esperado

Ao final do desafio o usuário deverá possuir:

✅ Uma planilha funcional

✅ Simulador de patrimônio

✅ Simulador de dividendos

✅ Dashboard visual

✅ Projeto documentado

✅ Repositório GitHub público

✅ Entrega realizada na plataforma DIO

------

# 🚀 Sugestões para Evolução do Projeto

Caso queira destacar seu projeto além do esperado pela DIO, considere implementar:

## Nível 1

- Gráficos dinâmicos
- Segmentação por perfil de investidor
- Simulação de inflação

------

## Nível 2

- Power Query
- Atualização automática de dados
- Importação de cotações

------

## Nível 3

- Integração com Power BI
- Dashboards executivos
- Indicadores financeiros avançados

------

## Nível 4

- Integração com Python
- Machine Learning
- IA Generativa para recomendações financeiras

------

# ☕ Dica Bellacosa Mainframe

Se você vem do mundo Mainframe, pense nesta solução exatamente como um sistema corporativo:

Entrada de Dados → Processamento → Regras de Negócio → Relatórios

A única diferença é que, neste laboratório, o Excel assume o papel que normalmente seria desempenhado por programas COBOL, tabelas DB2 e relatórios batch.

A lógica de negócio continua sendo a mesma utilizada há décadas nos grandes sistemas financeiros do mercado.

"Antes de investir dinheiro, invista conhecimento."