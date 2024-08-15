
Sumário

* [1. Introdução](#1-introdução)
    * [1.1 Pesquisa Exploratória](#11-pesquisa-exploratória)
    * [1.2 Pesquisa Desk](#12-pesquisa-desk)
* [2. Configurações Iniciais](#2-configurações-iniciais)
* [3. Solução Proposta](#3-solução-proposta)
    * [3.1 Mapeamento de Macroprocessos; Processos; Sub Processos](#31-mapeamento-de-macroprocessos-processos-sub-processos)
    * [3.2 Procedimentos e Regras de Negócios](#32-procedimentos-e-regras-de-negócios)
        * [3.2.1 Remanejamento de Estoque Local](#321-remanejamento-de-estoque-local)
        * [3.2.2 Vendas](#322-vendas)
        * [3.2.3 Pós-Venda](#323-pós-venda)
        * [3.2.4 Regras de Negócio Parametrizadas e Testes Unitários do Sistema](#324-regras-de-negócio-parametrizadas-e-testes-unitários-do-sistema)
    * [3.3 Fluxos de Processos](#33-fluxos-de-processos)
        * [3.3.1 Fluxos Pré-Vendas](#331-fluxos-pré-vendas)
        * [3.3.2 Fluxos de Vendas](#332-fluxos-de-vendas)
        * [3.3.3 Fluxos Pós-Vendas](#333-fluxos-pós-vendas)
* [4. Análise dos Dados Mestres](#4-análise-dos-dados-mestres)
    * [4.1 Dados de Escritório](#41-dados-de-escritório)
    * [4.2 Plano de Contas, Dados Contábeis e Bancários](#4.2-plano-de-contas)
    * [4.3 Dados dos Vendedores](#43-dados-dos-vendedores)
    * [4.4 Dados dos Clientes](#44-dados-dos-clientes)
    * [4.5 Dados dos Fornecedores](#45-dados-dos-fornecedores)
    * [4.6 Itens](#46-itens)
    * [4.7 DTW](#47-dtw)
* [5. Treinamento do SAP Business One - Módulo de Vendas](#5-treinamento-do-sap-business-one---módulo-de-vendas)

# 1. Introdução

## 1.1 Pesquisa Exploratória

## 1.2 Pesquisa Desk

### Introdução

&emsp;&emsp;Com o crescimento exponencial do uso de sistemas integrados de gestão empresarial (ERP) em todo o mundo, empresas de todos os portes buscam soluções para automatizar e otimizar seus fluxos de trabalho complexos. Considerando o cenário atual, 77% das transações ocorridas em todo o mundo passam por um sistema SAP[1], evidenciando a relevância dessa tecnologia no ambiente de negócios global. No caso de uma loja de roupas com operação online, sistemas como o SAP Business One desempenham um papel crucial ao integrar todos os dados da empresa em um único banco de dados, permitindo que processos como verificação de estoque, confirmação de pagamento, emissão de notas fiscais e comunicação com o cliente sejam realizados de forma rápida e automatizada. Esta pesquisa examina os benefícios da implementação do SAP Business One, abordando como ele transforma a gestão empresarial, reduzindo a complexidade e aumentando a eficiência operacional.

&emsp;&emsp;Posto isso, essa pesquisa tem como objetivo buscar dados referentes aos prováveis impactos da implantação do sistema ERP Sap Business One. Com isso, será possível avaliar a aplicabilidade da mesma solução na empresa G2 Tecnologia.

### Justificativa

&emsp;&emsp;A pesquisa é fundamental para justificar a implementação do sistema ERP, como o SAP Business One, pois é necessário compreender os impactos potenciais de seu uso nos processos da empresa. Neste documento, a empresa G2 Tecnologia busca implementar o SAP Business One para administrar seus macroprocessos. Portanto, é essencial realizar essa pesquisa para identificar os benefícios e determinar se esse sistema atende adequadamente às necessidades da empresa ou se são necessárias soluções mais robustas.

### Metodologia

&emsp;&emsp;Essa pesquisa é baseada em artigos e publicações de sites diversos. Através do cruzamento dessas informações serão gerados _insights_ os quais serão aproveitados para justificar a implementação do sistema de ERP Sap Business One na empresa G2 Tecnologia. Desses artigos foram retirados dados para metrificar os impactos, sejam positivos ou negativos, dada a implementação do sistema citado em empresas de pequeno e médio porte. Ou seja, utilizar da _Desk Research_ é um passo essencial para o entendimento do cenário a ser trabalhado e para coleta de dados cruciais para a tomada de decisão durante a implantação de um sistema de ERP.

&emsp;&emsp;Vale ressaltar que a _Desk Research_ é a coleta e análise de informações já disponíveis em diversas fontes[2]. Isto é, não cabe a essa etapa a criação de novos dados, apenas entender estudos pré existentes. Nesse caso, no âmbito do uso de ERP's, seus principais impactos e a implementação destes em _warehouses_.

### Relatório de pesquisa

&emsp;&emsp;Para encontrar os dados, primeiramente foi preciso entender o que são ERP's[3]. Então, entendendo suas principais características, vantagens e desvantagens sobre seu uso. Com isso, foi possível adquirir conhecimento necessário para compreender possíveis impactos e consequências do uso desses sistemas para a administração de processos empresariais.

&emsp;&emsp;Após essa compreensão do conceito e das características do sistema, é possível tentar começar a a responder a questão principal dessa pesquisa. Primeiramente, precisa-se entender quais setores podem ser afetados pela implementação da solução, com isso, pôde-se utilizar um estudo de caso que cobrisse todos os setores de alguma empresa com um sistema ERP[4]. E então filtrar para especificamente o setor de _warehouse_ [5], considerando que esse é o foco de implementação do Grupo 4.

&emsp;&emsp;Por último, para afirmar ou não se o ERP SAP seria realmente o melhor sistema a ser implementado na empresa, foi realizado um estudo comparativo entre dois dos principais softwares de gestão de processos: o ERP SAP e outro concorrente[6]. O objetivo desse estudo foi analisar as características, funcionalidades e benefícios oferecidos por cada um desses sistemas, a fim de determinar qual deles seria mais adequado às necessidades e objetivos da empresa G2 Tecnologia.

&emsp;&emsp;Durante a pesquisa, foram considerados diversos critérios, como a capacidade de integração com outros sistemas, a flexibilidade para personalização, a facilidade de uso, a escalabilidade, o suporte técnico oferecido, entre outros. Além disso, foram analisados casos de sucesso, a fim de obter uma visão mais ampla sobre a eficácia e os resultados alcançados.

&emsp;&emsp;No entanto, é importante ressaltar que a escolha do sistema ERP mais adequado para a empresa G2 Tecnologia deve levar em consideração suas necessidades específicas, seu orçamento disponível e sua capacidade de implementação. Portanto, é recomendado que a empresa realize uma análise mais aprofundada, considerando também outros fatores relevantes, como o custo-benefício, a curva de aprendizado e a compatibilidade com os sistemas e processos já existentes.

### Dados encontrados

&emsp;&emsp;Primeiramente, o uso de sistemas de ERP impacta diretamente a gestão de uma empresa em diversas vertentes, desde seus processos principais aos processos secundários. Segundo Todorov [1], 77% das transações ocorridas em todo o mundo passam por um sistema SAP, evidenciando a relevância dessa tecnologia no ambiente de negócios global. No caso de uma loja de roupas, por exemplo, com operação online, sistemas como o SAP Business One desempenham um papel crucial ao integrar todos os dados da empresa em um único banco de dados, permitindo que processos como verificação de estoque, confirmação de pagamento, emissão de notas fiscais e comunicação com o cliente sejam realizados de forma rápida e automatizada.

&emsp;&emsp;A implementação do SAP Business One traz diversos benefícios para a gestão empresarial, reduzindo a complexidade e aumentando a eficiência operacional [3]. Além disso, destaca-se que a implementação de um sistema ERP como o SAP Business One pode trazer melhorias significativas em áreas como planejamento e controle de compras, integração com manutenção da planta, integração com catálogo de equipamentos e materiais da planta, e controle de documentos[4] Com isso, levando a uma melhora a operação do estoque. Com isso, a pesquisa comparativa realizada revelou que a implementação ERP's em _warehouses_ resultou em uma redução significativa do ciclo de entrada no estoque, de 3,71 dias para 1,02 dias, representando uma redução de 73% [1]. Além disso, houve uma redução do tempo de entrega para frete aéreo, de 9,94 dias para 4,29 dias, uma redução de 57%. A precisão do inventário também melhorou, passando de 98,34% para 99,52%. Houve uma redução significativa de erros operacionais que geravam reclamações de clientes, de 43% para 11%. A taxa de atendimento também apresentou melhora, passando de 82,3% para 86,3% [5].

&emsp;&emsp;Esses resultados estão alinhados com o estudo comparativo realizado por Schrijvers [6], que aponta o aumento de desempenho como a principal vantagem da implementação do ERP, seguido por disciplina, padronização, estabilidade e tomada de decisão.

&emsp;&emsp;Além disso, é importante també considerar outras soluções de ERP. Comparando os dois maiores sistemas do mercado, NetSuite e o SAP Business One, em termos de funcionalidades específicas:

- Consolidação financeira: O NetSuite oferece consolidação financeira robusta, enquanto o SAP Business One tem módulos financeiros amigáveis.
- Gerenciamento de estoque: O NetSuite tem gerenciamento de estoque em tempo real, enquanto o SAP Business One se destaca em vendas, fornecendo análises detalhadas.
- CRM: Ambos os sistemas têm CRM, mas o NetSuite se integra melhor com outros módulos. O SAP Business One se integra a aplicativos de terceiros.
- Relatórios e inteligência de negócios: Para relatórios e inteligência de negócios, o NetSuite tem ferramentas modernas que facilitam a análise de dados complexos. Os relatórios do SAP Business One podem ser menos atualizados em comparação.

### Análise dos resultados

&emsp;&emsp; Dados os resultados encontrados, justifica-se a aplicação da solução ERP Sap Business One. Isso porque, considerando as funcionalidades de soluções ERP, os resultados encontrados em outras empresas e o comparativo com outra grande solução do mercado, o uso desse sistema tornaria a administração dos processos empresariais na G2 Tecnologia mais eficientes e centralizados em uma única ferramenta. Assim, facilitando a identificação de possíveis problemas operacionais e mitigando erros processuais.

# 2. Configurações Iniciais

# 3. Solução Proposta

## 3.1 Mapeamento de Macroprocessos; Processos; Sub Processos

## 3.2 Procedimentos e Regras de Negócios

### 3.2.1 Remanejamento de Estoque Local

### 3.2.2 Vendas

### 3.2.3 Pós-Venda

### 3.2.4 Regras de Negócio Parametrizadas e Testes Unitários do Sistema

## 3.3 Fluxos de Processos

### 3.3.1 Fluxos Pré-Vendas

### 3.3.2 Fluxos de Vendas

### 3.3.3 Fluxos Pós-Vendas

# 4. Análise dos Dados Mestres

## 4.1 Dados de Escritório

## 4.2 Plano de Contas, Dados Contábeis e Bancários

## 4.3 Dados dos Vendedores

## 4.4 Dados dos Clientes

## 4.5 Dados dos Fornecedores

## 4.6 Itens

## 4.7 DTW

# 5. Treinamento do SAP Business One - Módulo de Vendas

# Bibliografia

1. TODOROV, Georgi. 61 Important SAP Stats and Facts [and Trends] in 2024. ThriveMyWay, 2023. Disponível em: https://thrivemyway.com/sap-stats/. Acesso em: 11 ago.

2. MINDMINERS. O que é Desk Research?. Disponível em: https://mindminers.com/blog/o-que-e-desk-research/. Acesso em: 13 ago. 2024.

3. PADILHA, T. C. C.; MARINS, F. A. S. Sistemas ERP: características, custos e tendências. Revista Produção, v. 15, n. 1, p. 102-113, jan./abr. 2005.

4. Souza de Jesus, S.; Gomes, F.; Santana, A.; Pimenta, I. (2023). A Importância do ERP em Empresas de Logística, o Caso de uma Organização de Médio Porte. Sapientiae (8) 2, 253-267. www.doi.org/10.37293/sapientiae82.06. Acesso em: 15 ago. 2024.

5. Au Yong, Hui Nee. Warehouse Management System and Business Performance: Case Study of a Regional Distribution Centre. Proceedings of the 7th International Conference on Operations and Supply Chain Management, 2007. Acesso em: 14 de agosto de 2024.

6. SCHRIJVERS, John. NetSuite vs SAP Business One: An In-Depth Comparison. Rsult,. Disponível em: https://www.selleruniverse.io/blog/netsuite-vs-sap-comparison-guide. Acesso em: 15 ago. 2024.