
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

&emsp;&emsp;A sessão de "Introdução" procura estabelecer uma visão de experiência de usuário,detalhando o processo de entendimento das interações e percepções dos usuários em relação ao produto ou serviço em desenvolvimento. A análise da experiência do usuário (UX) garante que o produto final atenda às necessidades e expectativas do público-alvo, sendo um fator crítico para o sucesso do projeto.

&emsp;&emsp;Nessa seção, o grupo terá dois focos específicos: Uma pesquisa exploratória e a pesquisa desk. A pesquisa exploratória visa adquirir um entendimento inicial sobre o tema em questão, o que foi obtido por meio de observações em campo e pelo primeiro contato com o parceiro durante o Kick-off, que se deu no dia 7 (sete) de agosto de 2024. Este tipo de pesquisa é fundamental para construir uma base sólida para as etapas subsequentes, conforme discutido por Brown (2019), que destaca a importância de uma fase exploratória robusta para a criação de produtos centrados no usuário.

&emsp;&emsp;A pesquisa desk, por sua vez, requer a coleta de dados secundários a partir de fontes confiáveis, como livros, periódicos, publicações oficiais e relatórios de institutos reconhecidos. O objetivo dessa etapa é complementar os dados obtidos na pesquisa exploratória e fornecer uma visão abrangente do contexto do projeto. A eficácia da pesquisa desk está amplamente documentada na literatura, como aponta o estudo de Kumar (2020), que enfatiza a importância de utilizar múltiplas fontes secundárias para enriquecer o entendimento sobre o tema. Os temas escolhidos pela equipe para conduzir a pesquisa desk estão alinhados com o objetivos do módulo em questão, ou seja, o módulo SAP e a área de estoque.

## 1.1 Pesquisa Exploratória

&emsp;&emsp;A pesquisa exploratória para implementar o SAP Business One na G2 visa identificar e analisar os principais desafios e necessidades no processo de migração para um sistema ERP (Enterprise Resource Planning). A G2, que atua no mercado de tecnologia desde 2010, busca, segundo o TAPI, otimizar seus processos operacionais e melhorar a gestão empresarial por meio da centralização e eficiência dos dados mestres, tais como clientes, produtos e fornecedores. A relevância dessa implantação é proporcionar uma integração mais eficiente entre as diferentes áreas da empresa, otimizar o uso de recursos e permitir uma tomada de decisão mais informada, além de garantir uma infraestrutura de TI mais robusta e adaptável.

&emsp;&emsp;A pesquisa conduzida em aula no dia 7 de agosto revelou alguns desafios significativos. Um dos principais é a ausência de um mapeamento completo dos processos em algumas áreas da empresa, o que pode complicar a integração e migração dos dados para o SAP Business One. Em particular, a falta de mapeamento na área de estoque foi identificada como um ponto crítico que precisa ser abordado para garantir uma transição bem-sucedida para o novo sistema. Além disso, é essencial que a empresa defina com clareza quais dados mestres precisam ser migrados. Embora a resposta à pergunta sobre esse tema indique que há um número limitado de cadastros a serem migrados e que uma lista específica será definida, a ausência dessa definição precisa representa um risco potencial para o andamento do projeto.

&emsp;&emsp;Outro ponto relevante identificado na pesquisa, direcionado especificamente para a área de estoque, é em relação às funcionalidades que são consideradas essenciais para o MVP do SAP Business One. A gestão de licenças de SAP e a necessidade de uma visão clara sobre o tempo que uma licença permanece em estoque até ser vendida foram destacadas como funcionalidades prioritárias. Isso demonstra uma preocupação com a gestão eficiente dos recursos e a necessidade de que o sistema ofereça suporte adequado para essas operações.

&emsp;&emsp;Adicionalmente, a pesquisa explorou como a G2 Tecnologia gerencia seus dados, realiza vendas e lida com fatores críticos para o negócio. Foi constatado que, atualmente, a empresa utiliza ferramentas básicas, como calculadoras, para precificação de projetos, mas reconhece a necessidade de implementar dashboards que proporcionem uma visualização mais detalhada e de fácil acesso para os vendedores. Essa necessidade aponta para uma estrutura organizacional que pode ser significativamente aprimorada com a adoção do ERP.
Também foi abordada a questão de quem realiza os testes unitários dentro da empresa. A resposta indicou que os usuários finais estão envolvidos nesses testes, o que é positivo, pois garante que o sistema esteja alinhado com as necessidades reais de quem o utilizará. Entretanto, a pesquisa também sugere uma possível resistência ou preocupação em relação à transparência e à eficácia desses testes, o que deve ser cuidadosamente gerido para evitar problemas durante a fase de implementação.

&emsp;&emsp;Em suma, a pesquisa exploratória realizada destaca tanto os desafios quanto oportunidades que a G2 enfrenta na implantação do SAP Business One. A definição clara dos dados mestres a serem migrados, o mapeamento completo dos processos e a identificação das funcionalidades essenciais para o MVP são etapas cruciais para o sucesso do projeto. Além disso, o envolvimento dos usuários finais nos testes e a melhoria na gestão de dados e vendas através de novas ferramentas são pontos que podem potencializar os benefícios esperados com a implementação do sistema ERP. Então, ao abordar cuidadosamente essas questões, será possível alcançar os objetivos e garantir uma transição eficaz para o novo sistema de gestão empresarial.

## 1.2 Pesquisa Desk

### Introdução

&emsp;&emsp;Com o crescimento exponencial do uso de sistemas integrados de gestão empresarial (ERP) em todo o mundo, empresas de todos os portes buscam soluções para automatizar e otimizar seus fluxos de trabalho complexos. Considerando o cenário atual, 77% das transações ocorridas em todo o mundo passam por um sistema SAP, evidenciando a relevância dessa tecnologia no ambiente de negócios global. No caso de uma loja de roupas com operação online, sistemas como o SAP Business One desempenham um papel crucial ao integrar todos os dados da empresa em um único banco de dados, permitindo que processos como verificação de estoque, confirmação de pagamento, emissão de notas fiscais e comunicação com o cliente sejam realizados de forma rápida e automatizada. Esta pesquisa examina os impactos específicos da implementação do SAP Business One, abordando como ele transforma a gestão empresarial, reduzindo a complexidade e aumentando a eficiência operacional.

&emsp;&emsp;Posto isso, essa pesquisa tem como objetivo buscar dados referentes aos prováveis impactos da implantação do sistema ERP Sap Business One. Com isso, será possível avaliar a aplicabilidade da mesma solução na empresa G2.

### Metodologia

&emsp;&emsp;Essa pesquisa é baseada em artigos e publicações de sites diversos. Através do cruzamento dessas informações serão gerados _insights_ os quais serão aproveitados para justificar a implementação do sistema de ERP Sap Business One na empresa G2. Desses artigos foram retirados dados para metrificar os impactos, sejam positivos ou negativos, dada a implementação do sistema citado em empresas de pequeno e médio porte. Ou seja, utilizar da _Desk Research_ é um passo essencial para


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
