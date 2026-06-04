# 📊 FormulaExcel.md

# Principais Fórmulas Excel Utilizadas no Projeto de Controle de Investimentos

## 📖 Introdução

Este documento apresenta as principais fórmulas do Microsoft Excel utilizadas na construção da ferramenta de simulação de investimentos.

Além da sintaxe, são apresentados:

- Objetivo da fórmula
- Parâmetros
- Exemplos práticos
- Aplicações financeiras
- Casos de uso no projeto

------

# 💰 1. SOMA

## Para que serve?

Realiza a soma de valores numéricos.

## Sintaxe

```excel
=SOMA(número1; número2; ...)
```

## Exemplo

```excel
=SOMA(B2:B12)
```

## Resultado

Soma todos os valores entre B2 e B12.

## Aplicação no Projeto

- Total investido
- Soma de aportes
- Acumulação mensal

------

# 📈 2. MÉDIA

## Para que serve?

Calcula a média aritmética dos valores.

## Sintaxe

```excel
=MÉDIA(intervalo)
```

## Exemplo

```excel
=MÉDIA(C2:C13)
```

## Aplicação

- Média de dividendos
- Média de rentabilidade
- Média de aportes

------

# 📉 3. MÁXIMO

## Para que serve?

Retorna o maior valor encontrado.

## Sintaxe

```excel
=MÁXIMO(intervalo)
```

## Exemplo

```excel
=MÁXIMO(D2:D100)
```

## Aplicação

- Melhor rendimento
- Maior patrimônio

------

# 📉 4. MÍNIMO

## Para que serve?

Retorna o menor valor encontrado.

## Sintaxe

```excel
=MÍNIMO(intervalo)
```

## Aplicação

- Menor rendimento
- Menor patrimônio

------

# 💵 5. SE

## Para que serve?

Executa testes lógicos.

## Sintaxe

```excel
=SE(teste_lógico; valor_se_verdadeiro; valor_se_falso)
```

## Exemplo

```excel
=SE(B2>=1000;"Investimento Ideal";"Aumentar Aporte")
```

## Aplicação

Classificação automática do investidor.

------

# 📊 6. SES

## Para que serve?

Permite múltiplas condições.

## Sintaxe

```excel
=SES(
condição1;resultado1;
condição2;resultado2;
condição3;resultado3)
```

## Exemplo

```excel
=SES(
B2<500;"Conservador";
B2<1500;"Moderado";
VERDADEIRO;"Agressivo")
```

## Aplicação

Perfil de investidor.

------

# 💰 7. VF (Valor Futuro)

## Para que serve?

Calcula o valor futuro de um investimento.

## Sintaxe

```excel
=VF(taxa;nper;pgto;vp;tipo)
```

## Parâmetros

| Parâmetro | Descrição            |
| --------- | -------------------- |
| taxa      | Taxa de juros        |
| nper      | Número de períodos   |
| pgto      | Pagamento periódico  |
| vp        | Valor presente       |
| tipo      | Momento do pagamento |

------

## Exemplo

```excel
=VF(0,008;120;-500;0;0)
```

## Aplicação

Simular patrimônio acumulado após vários anos.

------

# 🏦 8. VP (Valor Presente)

## Para que serve?

Calcula quanto vale hoje um valor futuro.

## Sintaxe

```excel
=VP(taxa;nper;pgto;vf;tipo)
```

## Exemplo

```excel
=VP(0,008;120;0;500000)
```

## Aplicação

Planejamento financeiro.

------

# 📅 9. NPER

## Para que serve?

Calcula quantos períodos são necessários para atingir um objetivo.

## Sintaxe

```excel
=NPER(taxa;pgto;vp;vf;tipo)
```

## Exemplo

```excel
=NPER(0,008;-500;0;1000000)
```

## Aplicação

Descobrir em quanto tempo será alcançado R$ 1 milhão.

------

# 📈 10. TAXA

## Para que serve?

Calcula a taxa necessária para atingir um resultado.

## Sintaxe

```excel
=TAXA(nper;pgto;vp;vf)
```

## Aplicação

Simulações de rentabilidade.

------

# 💲 11. PGTO

## Para que serve?

Calcula o valor do aporte necessário.

## Sintaxe

```excel
=PGTO(taxa;nper;vp;vf)
```

## Exemplo

```excel
=PGTO(0,008;240;0;1000000)
```

## Aplicação

Determinar quanto investir por mês.

------

# 📊 12. PROCV

## Para que serve?

Busca informações em tabelas.

## Sintaxe

```excel
=PROCV(valor_procurado;tabela;coluna;falso)
```

## Exemplo

```excel
=PROCV("MXRF11";A2:D100;3;FALSO)
```

## Aplicação

Consulta de FIIs.

------

# 🔍 13. PROCX (Excel Moderno)

## Para que serve?

Substitui o PROCV.

## Sintaxe

```excel
=PROCX(valor;procurar_em;retornar)
```

## Exemplo

```excel
=PROCX(A2;Tabela[Código];Tabela[DY])
```

## Aplicação

Busca dinâmica de informações.

------

# 📈 14. SOMASE

## Para que serve?

Soma valores mediante condição.

## Sintaxe

```excel
=SOMASE(intervalo;critério;intervalo_soma)
```

## Exemplo

```excel
=SOMASE(A:A;"FII";B:B)
```

## Aplicação

Somar investimentos por categoria.

------

# 📊 15. CONT.SE

## Para que serve?

Conta ocorrências.

## Sintaxe

```excel
=CONT.SE(intervalo;critério)
```

## Aplicação

Quantidade de investimentos.

------

# 📉 16. ARRED

## Para que serve?

Arredonda números.

## Sintaxe

```excel
=ARRED(número;casas)
```

## Exemplo

```excel
=ARRED(B2;2)
```

------

# 💹 17. CAGR (Taxa de Crescimento)

## Fórmula Manual

```excel
=(VF/VI)^(1/ANOS)-1
```

## Exemplo

```excel
=(500000/100000)^(1/10)-1
```

## Aplicação

Analisar crescimento médio anual.

------

# 🏢 18. Dividend Yield

## Fórmula

```excel
=DIVIDENDOS/COTA
```

## Exemplo

```excel
=0,80/100
```

## Aplicação

Análise de Fundos Imobiliários.

------

# 📈 19. Rentabilidade

## Fórmula

```excel
=(ValorFinal-ValorInicial)/ValorInicial
```

## Aplicação

Medir retorno percentual.

------

# 💰 20. Dividendos Mensais

## Fórmula

```excel
=Patrimonio*DY
```

## Exemplo

```excel
=500000*0,008
```

## Resultado

```text
R$ 4.000 por mês
```

------

# 🚀 Fórmulas Avançadas Recomendadas

## FILTRO

```excel
=FILTRO(Tabela;Condição)
```

------

## ÚNICO

```excel
=ÚNICO(intervalo)
```

------

## CLASSIFICAR

```excel
=CLASSIFICAR(intervalo)
```

------

## LET

```excel
=LET(...)
```

Permite criar fórmulas mais organizadas.

------

## LAMBDA

```excel
=LAMBDA(...)
```

Permite criar funções personalizadas.

------

# 🎯 Fórmulas Essenciais para o Desafio

Se o objetivo for reproduzir integralmente a solução proposta pela DIO, as fórmulas mais importantes são:

✅ SOMA

✅ MÉDIA

✅ SE

✅ SOMASE

✅ VF

✅ VP

✅ NPER

✅ PGTO

✅ TAXA

✅ PROCV ou PROCX

✅ Dividend Yield

✅ Rentabilidade

✅ Dividendos Mensais

------

# ☕ Dica Bellacosa Mainframe

Em um ambiente corporativo, essas fórmulas representam regras de negócio que normalmente seriam implementadas em:

- COBOL
- PL/I
- Java
- Python
- C#

O Excel funciona como um pequeno sistema financeiro capaz de executar cálculos complexos sem a necessidade de programação tradicional.

Dominar essas fórmulas é equivalente a compreender a lógica de processamento utilizada por sistemas bancários, seguradoras e corretoras de investimento.