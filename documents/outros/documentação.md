
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

&emsp;&emsp;Com o crescimento exponencial do uso de sistemas integrados de gestão empresarial (ERP) em todo o mundo, empresas de todos os portes buscam soluções para automatizar e otimizar seus fluxos de trabalho complexos. Considerando o cenário atual, 77% das transações ocorridas em todo o mundo passam por um sistema SAP<sup><a href="#referencia-1">1</a></sup>, evidenciando a relevância dessa tecnologia no ambiente de negócios global. No caso de uma loja de roupas com operação online, sistemas como o SAP Business One desempenham um papel crucial ao integrar todos os dados da empresa em um único banco de dados, permitindo que processos como verificação de estoque, confirmação de pagamento, emissão de notas fiscais e comunicação com o cliente sejam realizados de forma rápida e automatizada. A primeira parte desta pesquisa examina os benefícios da implementação do SAP Business One, abordando como ele transforma a gestão empresarial, reduzindo a complexidade e aumentando a eficiência operacional. A segunda parte dela foca na área de estoque, a área em que a equipe em questão tem enfoque dentro da extensão de implantação geral, explorando a sua existência e relevância para o universo empreesarial, com um enfoque maior em como as tecnologias de sistemas integrados de gestão podem agir para a facilitação dessa área, visando o crescimento de uma empresa completa a partir disso.

&emsp;&emsp;Posto isso, essa pesquisa tem como objetivo buscar dados referentes aos prováveis impactos da implantação do sistema ERP *Sap Business One*. Com isso, será possível avaliar a aplicabilidade da mesma solução na empresa *G2 Tecnologia*.

### Justificativa

&emsp;&emsp;A pesquisa é fundamental para justificar a implementação do sistema ERP, como o *SAP Business One*, pois é necessário compreender os impactos potenciais de seu uso nos processos da empresa. Neste documento, a empresa G2 Tecnologia busca implementar o *SAP Business One* para administrar seus macroprocessos. Portanto, é essencial realizar essa pesquisa para identificar os benefícios e determinar se esse sistema atende adequadamente às necessidades da empresa ou se são necessárias soluções mais robustas.

### Metodologia

&emsp;&emsp;Essa pesquisa é baseada em artigos e publicações de sites diversos. Através do cruzamento dessas informações serão gerados _insights_ os quais serão aproveitados para justificar a implementação do sistema de ERP *Sap Business One* na empresa *G2 Tecnologia*. Desses artigos foram retirados dados para metrificar os impactos, sejam positivos ou negativos, dada a implementação do sistema citado em empresas de pequeno e médio porte. Ou seja, utilizar da _Desk Research_ (ou Pesquisa Desk) é um passo importante para o entendimento do cenário a ser trabalhado e para coleta de dados cruciais para a tomada de decisão durante a implantação de um sistema de ERP. A pesquisa foi dividida em duas etapas, as duas com suas questões direcionadoras que procuram relacionar o projeto a ser realizado pela equipe com uma pesquisa aprofundada sobre temas relacionadas à ERP e a área de estoque, são elas:

&emsp;&emsp;**Questão direcionadora 1:** Quais são os impactos e benefícios da implementação do sistema ERP SAP Business One para a gestão de processos empresariais, com ênfase na área de estoque, na empresa G2 Tecnologia?

&emsp;&emsp;**Questão direcionadora 2:** O que é um estoque e como ele afeta os resultados das empresas e como sistemas ERP (enterprise resource planning) podem melhorar o desempenho dele?

&emsp;&emsp;Vale ressaltar que a Pesquisa Desk é a coleta e análise de informações já disponíveis em diversas fontes<sup><a href="#referencia-2">2</a></sup>. Isto é, não cabe a essa etapa a criação de novos dados, apenas entender estudos pré existentes. Nesse caso, no âmbito do uso de ERP's, seus principais impactos e a implementação destes em _warehouses_.

### Questão direcionadora 1

**Relatório de pesquisa**

&emsp;&emsp;Para encontrar os dados, primeiramente foi preciso entender o que são ERP's<sup><a href="#referencia-3">3</a></sup>. Então, entendendo suas principais características, vantagens e desvantagens sobre seu uso. Com isso, foi possível adquirir conhecimento necessário para compreender possíveis impactos e consequências do uso desses sistemas para a administração de processos empresariais.

&emsp;&emsp;Após essa compreensão do conceito e das características do sistema, é possível tentar começar a a responder a questão principal dessa pesquisa. Primeiramente, precisa-se entender quais setores podem ser afetados pela implementação da solução, com isso, pôde-se utilizar um estudo de caso que cobrisse todos os setores de alguma empresa com um sistema ERP<sup><a href="#referencia-4">4</a></sup>. E então filtrar para especificamente o setor de _warehouse_ <sup><a href="#referencia-5">5</a></sup>, considerando que esse é o foco de implementação do Grupo 4.

&emsp;&emsp;Por último, para afirmar ou não se o ERP SAP seria realmente o melhor sistema a ser implementado na empresa, foi realizado um estudo comparativo entre dois dos principais softwares de gestão de processos: o ERP SAP e outro concorrente<sup><a href="#referencia-6">6</a></sup>. O objetivo desse estudo foi analisar as características, funcionalidades e benefícios oferecidos por cada um desses sistemas, a fim de determinar qual deles seria mais adequado às necessidades e objetivos da empresa G2 Tecnologia.

&emsp;&emsp;Durante a pesquisa, foram considerados diversos critérios, como a capacidade de integração com outros sistemas, a flexibilidade para personalização, a facilidade de uso, a escalabilidade, o suporte técnico oferecido, entre outros. Além disso, foram analisados casos de sucesso, a fim de obter uma visão mais ampla sobre a eficácia e os resultados alcançados.

&emsp;&emsp;No entanto, é importante ressaltar que a escolha do sistema ERP mais adequado para a empresa G2 Tecnologia deve levar em consideração suas necessidades específicas, seu orçamento disponível e sua capacidade de implementação. Portanto, é recomendado que a empresa realize uma análise mais aprofundada, considerando também outros fatores relevantes, como o custo-benefício, a curva de aprendizado e a compatibilidade com os sistemas e processos já existentes.

**Dados encontrados**

&emsp;&emsp;Primeiramente, o uso de sistemas de ERP impacta diretamente a gestão de uma empresa em diversas vertentes, desde seus processos principais aos processos secundários. Segundo Todorov (2023)<sup><a href="#referencia-1">1</a></sup>, 77% das transações ocorridas em todo o mundo passam por um sistema SAP, evidenciando a relevância dessa tecnologia no ambiente de negócios global. No caso de uma loja de roupas, por exemplo, com operação online, sistemas como o SAP Business One desempenham um papel crucial ao integrar todos os dados da empresa em um único banco de dados, permitindo que processos como verificação de estoque, confirmação de pagamento, emissão de notas fiscais e comunicação com o cliente sejam realizados de forma rápida e automatizada.

&emsp;&emsp;A implementação do *SAP Business One* traz diversos benefícios para a gestão empresarial, reduzindo a complexidade e aumentando a eficiência operacional <sup><a href="#referencia-3">3</a></sup>. Além disso, destaca-se que a implementação de um sistema ERP como o *SAP Business One* pode trazer melhorias significativas em áreas como planejamento e controle de compras, integração com manutenção da planta, integração com catálogo de equipamentos e materiais da planta, e controle de documentos<sup><a href="#referencia-4">4</a></sup> Com isso, levando a uma melhora a operação do estoque. Com isso, a pesquisa comparativa realizada revelou que a implementação ERP's em _warehouses_ resultou em uma redução significativa do ciclo de entrada no estoque, de 3,71 dias para 1,02 dias, representando uma redução de 73% <sup><a href="#referencia-1">1</a></sup>. Além disso, houve uma redução do tempo de entrega para frete aéreo, de 9,94 dias para 4,29 dias, uma redução de 57%. A precisão do inventário também melhorou, passando de 98,34% para 99,52%. Houve uma redução significativa de erros operacionais que geravam reclamações de clientes, de 43% para 11%. A taxa de atendimento também apresentou melhora, passando de 82,3% para 86,3% <sup><a href="#referencia-5">5</a></sup>.

&emsp;&emsp;Esses resultados estão alinhados com o estudo comparativo realizado por Schrijvers (2023)<sup><a href="#referencia-6">6</a></sup>, que aponta o aumento de desempenho como a principal vantagem da implementação do ERP, seguido por disciplina, padronização, estabilidade e tomada de decisão.

&emsp;&emsp;Além disso, é importante também considerar outras soluções de ERP. Comparando os dois maiores sistemas do mercado, NetSuite e o *SAP Business One*, em termos de funcionalidades específicas:

- Consolidação financeira: O NetSuite oferece consolidação financeira robusta, enquanto o *SAP Business One* tem módulos financeiros amigáveis.
- Gerenciamento de estoque: O NetSuite tem gerenciamento de estoque em tempo real, enquanto o *SAP Business One* se destaca em vendas, fornecendo análises detalhadas.
- CRM: Ambos os sistemas têm CRM, mas o NetSuite se integra melhor com outros módulos. O *SAP Business One* se integra a aplicativos de terceiros.
- Relatórios e inteligência de negócios: Para relatórios e inteligência de negócios, o NetSuite tem ferramentas modernas que facilitam a análise de dados complexos. Os relatórios do *SAP Business One* podem ser menos atualizados em comparação.

&emsp;&emsp; Dados os resultados encontrados, justifica-se a aplicação da solução ERP *Sap Business One*. Isso porque, considerando as funcionalidades de soluções ERP, os resultados encontrados em outras empresas e o comparativo com outra grande solução do mercado, o uso desse sistema tornaria a administração dos processos empresariais na G2 Tecnologia mais eficientes e centralizados em uma única ferramenta. Assim, facilitando a identificação de possíveis problemas operacionais e mitigando erros processuais.

### Questão direcionadora 2

**Relatório de pesquisa**

&emsp;&emsp;Com técnica semelhante à descrita anteriormente, a Pesquisa Desk na questão direcionadora dois tem como objetivo objetificar um tema – Qual é a relevância do estoque nas empresas e como sistemas gerenciais podem melhorar os resultados da empresa? – dentro de gestão empresarial com enfoque na área de estoque. A equipe tem como objetivo revelar a importância dessa área, bem como os seus pontos de força e fraqueza, e a partir disso oferecer uma visão clara de como os métodos utilizados de forma usual, como planilhas, podem afetar o avanço de uma empresa, fazendo-a perder cenários dentro do mercado, e como os sistemas ERP podem atuar a partir disso dentro da área de estoque.

**Dados encontrados**

&emsp;&emsp;É importante iniciar a presente pesquisa destacando a importância de uma área de estoque dentro de um contexto de empresa. Segundo o blog da ContaAzul (2024)<sup><a href="#referencia-7">7</a></sup> em seu artigo “O que é estoque?”, os benefícios de uma boa gestão de estoque podem ser percebidos em diferentes áreas, como: financeiro, satisfação do cliente, vendas e fluxo produtivo. Em cada uma delas, existe uma vantagem a ser destacada. Dentro do financeiro, temos a rotatividade correta de produtos, a contabilização correta de compras, e a garantia de que as vendas realizadas serão entregues; Já em outras áreas, podemos enxergar benefícios como satisfação por agilidade e eficiência em entregas e processos, aumento da produtividade em atendimentos, vendas garantidas ou clientes prospectados por noção de estoque dos produtos e mais.  

&emsp;&emsp;Tendo os benefícios em mente, é interessante entender como funcionam os subprocessos que pertencem ao ambiente de estocagem. Com isso, é possível entender como esses benefícios são gerados e onde, exatamente, os resultados das empresas são impactados. Segundo a revista Exame (2022)<sup><a href="#referencia-7">7</a></sup>, as tarefas referentes ao controle de estoque são: a realização de um inventário de estoque por meio de uma tabela padronizada; a automatização do controle desses estoque para obter a contabilização de entradas e saídas; o treinamento dos colaboradores; a adoção de estratégias para melhorar a rotatividade de mercadorias; determinar a perda aceitável; calcular os custos de armazenamento; buscar estratégias de redução de prejuízos e a preparação dos pedidos para entrega. Sabendo dessa informação, podemos concluir então que possivelmente os resultados são impactados através da prevenção de perda e na metrificação de custos de fato necessários com a mercadoria. 

&emsp;&emsp;Ou seja, ao garantir a mobilidade de produtos, verificação de disponibilidade de materiais e controle de qualidade dos ativos da companhia, o estoque se torna uma chave importante em empresas, que dependem dele para previsões de outras áreas – como compras, vendas, financeiro e contábil – tornando o estoque uma área suporte que pretende atender diversos setores de uma empresa específica, melhorando dessa forma o desempenhos da organização e protegendo recursos valiosos, como tempo, força de trabalho e dinheiro, mas tendo igual poder, quando não administrada de forma eficiente, de causar a perda de bens.

&emsp;&emsp;Dada a importância da área de estoque para empresas, evidencia-se a necessidade de haver um sistema gerencial eficiente por trás do controle de estoque. Uma diversidade de empresas, principalmente de pequeno e médio porte, possuem o seu controle interno por meio de tecnologias não propícias e/ou ineficientes. Bavaresco (2024)<sup><a href="#referencia-11">11</a></sup> defende que a medida que os negócios se tornaram mais dinâmicos e as demandas por eficiência e precisão aumentaram, as limitações intrínsecas das planilhas, ferramenta ainda muito utilizada para controle de estoque, começaram a se destacar, por diversos motivos, sendo alguns deles a dificuldade em lidar com grandes volumes de dados, a ausência de funcionalidades colaborativas e a falta de controle de segurança. E uma das principais dificuldades, segundo Bavaresco, seria o controle de escalabilidade, pois lutam para gerenciar de forma eficiente volumes amplos de dados, que aumentam proporcionalmente com o tamanho de uma empresa, tornando inviável a continuidade de sua implementação em negócios que pretendem escalar e ampliar-se dentro do mercado, sendo um impeditivo para a conquista de novos cenários, bem como para a melhoria de eficiência dentro do contexto de escopo atual.

&emsp;&emsp;A solução para isso seria, primeiramente, compreender os processos internos da empresa em questão, segundo Nóbile (2016)<sup><a href="#referencia-12">12</a></sup>, o mapeamento de processos auxilia a assimilar o funcionamento dos aspectos internos da empresa, ou seja entender como o processo funciona na prática, para isso existem diversas técnicas específicas, denominadas mineração de processos como o Mapa de processos de negócios (BPMN), Mapa de cadeia de valor (VSM) ou o SIPOC (Suppliers, Inputs, Outputs, Customers). Quando compreende-se os fluxos com assertividade, é possível, entre outros pontos, decifrar as necessidades intraorganizacionais e escolher a ferramenta de gerenciamento que atende a essas necessidades. Segundo o site oficial do SAP Extended Warehouse Management (SAP EWM), algumas das vantagens intrínsecas de utilizar sistemas de gestão para o cenário de estoque são: processos de qualidade, produção, rastreamento e controle totalmente integrados, controle direto de equipamentos de automação de depósitos e regras inteligentes de planejamento do armazenamento para otimizar a utilização de espaço.

&emsp;&emsp;Dessa forma, a presente pesquisa realizada evidencia a relevância da gestão de estoque dentro do ambiente empresarial, demonstrando que o controle eficiente dessa área impacta diretamente diversos setores. A análise dos processos internos de estocagem mostra que a gestão adequada não apenas otimiza a operação da empresa, mas também previne perdas e facilita a tomada de decisões estratégicas. No entanto, a pesquisa também aponta as limitações das ferramentas tradicionais, como planilhas, que muitas vezes são incapazes de acompanhar o crescimento e as demandas complexas das empresas modernas.

&emsp;&emsp;Diante disso, a implementação de sistemas de gestão empresarial, como o ERP SAP Business One, surge como uma solução essencial para melhorar a eficiência e a precisão do controle de estoque. Esses sistemas oferecem funcionalidades avançadas que permitem uma gestão integrada e otimizada, atendendo às necessidades de escalabilidade e segurança que são fundamentais para empresas que buscam crescimento e competitividade no mercado.


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

# 5. Treinamento do *SAP Business One* - Módulo de Vendas

# Bibliografia

1. <a name="referencia-1"></a> TODOROV, Georgi. 61 Important SAP Stats and Facts [and Trends] in 2024. ThriveMyWay, 2023. Disponível em: https://thrivemyway.com/sap-stats/. Acesso em: 11 ago.

2. <a name="referencia-2"></a> MINDMINERS. O que é Desk Research?. Disponível em: https://mindminers.com/blog/o-que-e-desk-research/. Acesso em: 13 ago. 2024.

3. <a name="referencia-3"></a> PADILHA, T. C. C.; MARINS, F. A. S. Sistemas ERP: características, custos e tendências. Revista Produção, v. 15, n. 1, p. 102-113, jan./abr. 2005.

4. <a name="referencia-4"></a> Souza de Jesus, S.; Gomes, F.; Santana, A.; Pimenta, I. (2023). A Importância do ERP em Empresas de Logística, o Caso de uma Organização de Médio Porte. Sapientiae (8) 2, 253-267. www.doi.org/10.37293/sapientiae82.06. Acesso em: 15 ago. 2024.

5. <a name="referencia-5"></a> Au Yong, Hui Nee. Warehouse Management System and Business Performance: Case Study of a Regional Distribution Centre. Proceedings of the 7th International Conference on Operations and Supply Chain Management, 2007. Acesso em: 14 de agosto de 2024.

6. <a name="referencia-6"></a> SCHRIJVERS, John. NetSuite vs SAP Business One: An In-Depth Comparison. Rsult,. Disponível em: https://www.selleruniverse.io/blog/netsuite-vs-sap-comparison-guide. Acesso em: 15 ago. 2024.

7. EXAME, Da Redação. Controle de estoque: o que é, exemplos e como fazer?. Redação Exame, 29 jul. 2022. Disponível em: <https://exame.com/invest/guia/controle-de-estoque-o-que-e-para-que-serve-e-como-funciona/>. Acesso em: 12 ago. 2024.

8. SOUSA, Diego Camilo Ferreira; CLAUDINO, Calline Neves de Queiroz; AQUINO, Joás Tomaz de; MELO, Fagner José Coutinho de. Utilização de ferramentas gerenciais para o controle de estoques: Um estudo de caso de uma empresa do setor alimentício. GESTÃO.Org, v. 15, n. 2, p. 546-563, 2017. ISSN-e 1679-1827. Disponível em: <https://dialnet.unirioja.es/servlet/articulo?codigo=7326517>. Acesso em: 14 ago. 2024.

9. INTELIGÊNCIA ARTIFICIAL NA GESTÃO DE ESTOQUE. Fateclog, 2019. Disponível em: <https://fateclog.com.br/anais/2019/INTELIG%C3%8ANCIA%20ARTIFICIAL%20NA%20GEST%C3%83O%20DE%20ESTOQUE.pdf>. Acesso em: 11 ago. 2024.

10. EQUIPE CONTA AZUL. O que é estoque?. Conta Azul Blog, 26 jan. 2024. Disponível em: <https://blog.contaazul.com/glossario-estoque/>. Acesso em: 13 ago. 2024.

11. BAVARESCO, Fabiana. Gestão de Indicadores | KPIs. Scoreplan Blog, 1 abr. 2024. Disponível em: <https://scoreplan.com.br/blog/gestao-de-indicadores/>. Acesso em: 15 ago. 2024.

12. ALMEIDA, Vinicius Nóbile de. O que é e como fazer Mapeamento de Processos em 6 passos. Euax, 28 jun. 2016. Disponível em: <https://www.euax.com.br/2016/06/como-fazer-mapeamento-de-processos-em-6-passos/>. Acesso em: 12 ago. 2024.





