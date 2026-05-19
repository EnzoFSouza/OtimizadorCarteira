## Algoritmo Genético para Otimização de Carteiras de Investimentos
Projeto desenvolvido em Python utilizando Algoritmos Genéticos (AG) para otimização de carteiras de investimentos com diferentes perfis de investidor.
O sistema simula o processo evolutivo de seleção natural para encontrar distribuições de ativos que maximizam retorno e dividendos enquanto minimizam risco.

## Objetivo
Este projeto foi desenvolvido com fins de estudo em:
Inteligência Artificial
Algoritmos Genéticos
Otimização
Economia

O algoritmo cria populações de carteiras, avalia sua qualidade utilizando uma função de fitness e evolui as soluções ao longo das gerações utilizando:
- Seleção por torneio
- Crossover
- Mutação
- Elitismo
- Penalização por concentração

## Tecnologias Utilizadas
- Python
- Numpy
- Matplotlib

## Conceitos
Cada indivíduo da população representa uma carteira de investimentos: [0.10, 0.15, 0.05, 0.20, ...]
Onde cada valor representa o percentual investido em um ativo e a soma total dos pesos é sempre 1 (100%)

## Ativos Utilizados
O projeto utiliza ativos simulados:
Ações: PETR4, VALE3, ITUB4, WEGE3, BBAS3
FIIs: HGLG11, XPLG11, KNRI11, MXRF11, VISC11

## Perfis de Investidor
O algoritmo pode otimizar carteiras para diferentes perfis:
| Perfil      | Prioridade           |
| ----------- | -------------------- |
| Conservador | Menor risco          |
| Dividendos  | Maior dividend yield |
| Crescimento | Maior retorno        |

Cada perfil altera os pesos da função de fitness

## Função de Fitness
A função de fitness avalia a qualidade de cada carteira:
`score = retorno * peso_retorno + dividendos * peso_dividendos - risco * peso_risco`
O objetivo do algoritmo é:
- Maximizar retorno
- Maximizar dividendos
- Minimizar risco

## Penalização por Concentração
Foi adicionada uma penalização para evitar carteiras excessivamente concentradas em poucos ativos.
Sem penalização, o AG tende a
- Concentrar capital em 1 ou 2 ativos
- Minimizar os demais pesos

Com penalização:
- A carteira fica mais diversificada
- O portfólio se torna mais equilibrado

## Resultados
O projeto gera gráficos para análise da evolução do algoritmo:
- Comparação entre Perfis
- Evolução do fitness por geração
- Diferenças entre perfis de investidor
- Impacto do Elitismo

## Carteiras Finais
Distribuição percentual dos ativos para cada perfil.

## Exemplos de Gráficos
Evolução do Fitness
- Fitness aumenta ao longo das gerações
- O AG aprende soluções melhores progressivamente
- Distribuição Final da Carteira

Gráficos de pizza mostram:
- Percentual investido em cada ativo
- Diferença entre os perfis de investidor

## Autor
Desenvolvido por Enzo Florentino Souza.
Projeto desenvolvido para estudos em Inteligência Artificial, Algoritmos Genéticos e Otimização de Carteiras.
