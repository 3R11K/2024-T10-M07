
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

&emsp;&emsp;Com o crescimento exponencial do uso de sistemas integrados de gestão empresarial (ERP) em todo o mundo, empresas de todos os portes buscam soluções para automatizar e otimizar seus fluxos de trabalho complexos. Considerando o cenário atual, 77% das transações ocorridas em todo o mundo passam por um sistema SAP, evidenciando a relevância dessa tecnologia no ambiente de negócios global. No caso de uma loja de roupas com operação online, sistemas como o SAP Business One desempenham um papel crucial ao integrar todos os dados da empresa em um único banco de dados, permitindo que processos como verificação de estoque, confirmação de pagamento, emissão de notas fiscais e comunicação com o cliente sejam realizados de forma rápida e automatizada. Esta pesquisa examina os impactos específicos da implementação do SAP Business One, abordando como ele transforma a gestão empresarial, reduzindo a complexidade e aumentando a eficiência operacional.

&emsp;&emsp;Posto isso, essa pesquisa tem como objetivo buscar dados referentes aos prováveis impactos da implantação do sistema ERP Sap Business One. Com isso, será possível avaliar a aplicabilidade da mesma solução na empresa G2.

### Metodologia

&emsp;&emsp;Essa pesquisa é baseada em artigos e publicações de sites diversos. Através do cruzamento dessas informações serão gerados _insights_ os quais serão aproveitados para justificar a implementação do sistema de ERP Sap Business One na empresa G2. Desses artigos foram retirados dados para metrificar os impactos, sejam positivos ou negativos, dada a implementação do sistema citado em empresas de pequeno e médio porte. Ou seja, utilizar da _Desk Research_ é um passo essencial para

# 2. Configurações Iniciais

## 1) Informações básicas de configuração da empresa

Aqui serão inseridas informações sobre a empresa as quais serão úteis para tarefas como a geração de relatórios pelo SAP, dentre outros.

### 1.01) Nome da Empresa
**Descrição**: Esta seção refere-se à inserção das informações fundamentais que identificam a empresa dentro do sistema SAP. Isso inclui o nome oficial da empresa, que é utilizado em diversos relatórios e documentos fiscais.

### 1.02) Endereço da Empresa
**Descrição**: O endereço da empresa é uma informação crucial que será utilizada para fins fiscais, correspondências, e identificação em documentos oficiais emitidos pelo sistema.

**Caminho no SAP**: Para inserir o endereço da empresa, siga o caminho:
1. Acesse o menu "Administração" > "Configuração Geral".
2. Selecione "Configurações de Empresa" e, em seguida, "Informações Básicas".
3. Preencha os campos referentes ao endereço, incluindo Tipo Logradouro, Rua, Número, Complemento, CEP, Bairro, Distrito, Estado, Município e País.

**Status**: (sim/não)

**Justificativa**: (caso não, justificar)
### 1.03) Web
**Descrição**: Esta seção envolve a configuração do website oficial da empresa e dos principais e-mails de contato, que serão exibidos em documentos gerados pelo SAP.

**Caminho no SAP**: Para configurar o website e e-mails da empresa:
1. Acesse o menu "Administração" > "Configuração Geral".
2. Selecione "Configurações de Empresa" e, em seguida, "Informações Básicas".
3. Preencha os campos referentes ao site e e-mails.

**Status**:(sim/não)

**Justificativa**: (caso não, justificar)

### 1.04) Telefone
**Descrição**: O telefone da empresa é uma informação essencial para contato, que será utilizada em documentos, relatórios, e comunicação em geral.

**Caminho no SAP**: Para inserir o telefone da empresa:
1. Acesse o menu "Administração" > "Configuração Geral".
2. Selecione "Configurações de Empresa" e, em seguida, "Informações Básicas".
3. Insira o número de telefone principal e, se aplicável, outros números de contato.

**Status**: (Sim/Não)

**Justificativa**: (caso não, justificar)

### 1.05) Dados Contábeis
**Descrição**: Esta seção abrange as informações contábeis da empresa, como o CNPJ, a inscrição estadual e municipal, e outras informações fiscais essenciais para o correto funcionamento e conformidade do sistema SAP.

**Caminho no SAP**: Para configurar os dados contábeis:
1. Acesse o menu "Administração" > "Configuração Geral".
2. Selecione "Configurações de Empresa" e, em seguida, "Dados Contábeis".
3. Preencha os campos com as informações fiscais e contábeis da empresa.

**Status**: (Sim/Não)

**Justificativa**: (caso não, justificar)

### 1.06) Campos de Localização
**Descrição**: Os campos de localização permitem o registro de informações adicionais de localização e registro da empresa, como a data de incorporação e o perfil do SPED.

**Caminho no SAP**: Para configurar os campos de localização:
1. Acesse o menu "Administração" > "Configuração Geral".
2. Selecione "Configurações de Empresa" e, em seguida, "Campos de Localização".
3. Insira as informações pertinentes.

**Status**: (Sim/Não)

**Justificativa**: (caso não, justificar)

### 1.07) Caminho para pastas
**Descrição**: Nesta seção, são definidos os caminhos de pastas no servidor da empresa onde serão armazenados documentos e anexos relevantes para o funcionamento do SAP.

**Caminho no SAP**: Para configurar os caminhos de pastas:
1. Acesse o menu "Administração" > "Configuração Geral".
2. Selecione "Configurações de Empresa" e, em seguida, "Caminho para pastas".
3. Especifique os caminhos para pastas de arquivos do Word, Excel, imagens, anexos, licenças de add-ons, e arquivos XML.

**Status**: (Sim/Não)

**Justificativa**: (caso não, justificar)

## 2) Configurações gerais da empresa

 Esta seção permite configurar definições básicas e globais que afetam toda a operação do sistema, como formatos de data e hora, número de casas decimais, e métodos de atribuição de números de série e lotes.

### 2.01) Opções de alerta da atividade do cliente
**Descrição**: As opções de alerta configuram notificações automáticas dentro do sistema SAP com base em atividades específicas dos clientes, como limites de crédito e saldo de remessas.

**Caminho no SAP**: Para configurar as opções de alerta:
1. Acesse o menu "Administração" > "Configuração Geral".
2. Selecione "Configurações de Empresa" e, em seguida, "Opções de Alerta".
3. Configure as preferências de alertas de acordo com as políticas da empresa.

**Status**: (Sim/Não)

**Justificativa**: (caso não, justificar)

### 2.02) Com base em que seu negócio define a taxa de comissão, se aplicada?
**Descrição**: Esta configuração determina os critérios pelos quais as taxas de comissão serão calculadas no sistema SAP. Isso pode incluir fatores como vendedor, item vendido, ou cliente específico.

**Caminho no SAP**: Para configurar a taxa de comissão:
1. Acesse o menu "Administração" > "Configuração Geral".
2. Selecione "Configurações de Empresa" e, em seguida, "Taxa de Comissão".
3. Escolha os critérios de base para a definição da taxa de comissão.

**Status**: (Sim/Não)

**Justificativa**: (caso não, justificar)

### 2.03) Condições de Pagamento
**Descrição**: As condições de pagamento configuram os termos pelos quais a empresa gerencia os pagamentos de clientes e fornecedores, definindo prazos, descontos por pagamento antecipado, entre outros.

**Caminho no SAP**: Para configurar as condições de pagamento:
1. Acesse o menu "Administração" > "Configuração Geral".
2. Selecione "Configurações de Empresa" e, em seguida, "Condições de Pagamento".
3. Defina as condições de pagamento para clientes e fornecedores.

**Status**: (Sim/Não)

**Justificativa**: (caso não, justificar)

### 2.04) Qual formato de hora você gostaria de utilizar na exibição na tela
**Descrição**: Esta configuração permite definir o formato de hora (12h ou 24h) que será utilizado na interface do usuário e em relatórios gerados pelo sistema.

**Caminho no SAP**: Para definir o formato de hora:
1. Acesse o menu "Administração" > "Configuração Geral".
2. Selecione "Configurações de Empresa" e, em seguida, "Formato de Hora".
3. Escolha entre os formatos de 12 horas ou 24 horas.

**Status**: (Sim/Não)

**Justificativa**: (caso não, justificar)

### 2.05) Qual formato de data você gostaria de utilizar na exibição na tela
**Descrição**: Define como as datas serão exibidas na interface do usuário e em documentos gerados pelo sistema, podendo ser no formato DD/MM/AAAA, MM/DD/AAAA, etc.

**Caminho no SAP**: Para configurar o formato de data:
1. Acesse o menu "Administração" > "Configuração Geral".
2. Selecione "Configurações de Empresa" e, em seguida, "Formato de Data".
3. Escolha o formato de data desejado para exibição.

**Status**: (Sim/Não)

**Justificativa**: (caso não, justificar)

### 2.06) Quantas casas decimais você deseja exibir e utilizar em cálculos
**Descrição**: Define a quantidade de casas decimais que serão exibidas e utilizadas nos cálculos para preços, taxas, quantidades, e outras métricas dentro do sistema SAP.

**Caminho no SAP**: Para configurar as casas decimais:
1. Acesse o menu "Administração" > "Configuração Geral".
2. Selecione "Configurações de Empresa" e, em seguida, "Casas Decimais".
3. Defina o número de casas decimais para cada tipo de valor (preços, taxas, quantidades, etc.).

**Status**: (Sim/Não)

**Justificativa**: (caso não, justificar)

### 2.07) Selecione o método desejado para atribuir números de série e números administrados em lotes a itens
**Descrição**: Esta configuração permite determinar como o SAP deve gerenciar a numeração de série e a administração de lotes para itens, essencial para o controle de estoque e rastreabilidade.

**Caminho no SAP**: Para configurar a numeração de série e lotes:
1. Acesse o menu "Administração" > "Configuração Geral".
2. Selecione "Configurações de Empresa" e, em seguida, "Numeração de Série e Lotes".
3. Escolha o método de atribuição para números de série e lotes conforme as necessidades da empresa.

**Status**: (Sim/Não)

**Justificativa**: (caso não, justificar)

### 2.08) Adição automática de todos os depósitos a novos itens
**Descrição**: Esta configuração determina se todos os depósitos da empresa serão automaticamente associados a novos itens criados no sistema, facilitando a gestão de inventário.

**Caminho no SAP**: Para configurar a adição automática de depósitos:
1. Acesse o menu "Administração" > "Configuração Geral".
2. Selecione "Configurações de Empresa" e, em seguida, "Depósitos Automáticos".
3. Ative ou desative a opção conforme as necessidades da empresa.

**Status**: (Sim/Não)

**Justificativa**: (caso não, justificar)

## 3) Plano de Contas da Empresa

Esta seção define a estrutura contábil da empresa dentro do sistema SAP.

### 3.01) Forneça uma cópia atual do plano de contas de seu negócio em planilha do Excel
**Descrição**: Esta etapa requer que a empresa forneça uma cópia do seu plano de contas, essencial para a configuração contábil do sistema SAP. O plano de contas é utilizado para mapear as transações financeiras e garantir conformidade fiscal.

**Caminho no SAP**: Não se aplica uma configuração direta nesta etapa, mas o plano de contas deve ser revisado e importado para o sistema SAP conforme os procedimentos padrão de configuração contábil.

**Status**: (Sim/Não)

**Justificativa**: (caso não, justificar)

## 4) Definir informações de banco

### 4.01) Informe as contas bancárias da empresa
**Descrição**: Nesta seção, as contas bancárias da empresa são cadastradas no sistema SAP para permitir a automação de pagamentos, recebimentos e conciliações bancárias.

**Caminho no SAP**: Para cadastrar as informações de contas bancárias:
1. Acesse o menu "Administração" > "Configuração Financeira".
2. Selecione "Bancos" e, em seguida, "Contas Bancárias".
3. Preencha os dados da conta, como código do banco, número da agência, número da conta, e tipo de conta.

**Status**: (Sim/Não)

**Justificativa**: (caso não, justificar)

## 5) Determinação da conta contábil para lançamentos de transação

### 5.01) Vendas
**Descrição**: Esta seção abrange a configuração das contas contábeis utilizadas para registrar as transações de vendas. É essencial para garantir que todas as receitas e movimentações de contas relacionadas às vendas sejam devidamente registradas no sistema SAP.

**Caminho no SAP**: Para configurar as contas contábeis de vendas:
1. Acesse o menu "Administração" > "Configuração Financeira".
2. Selecione "Determinação de Contas Contábeis" e, em seguida, "Vendas".
3. Configure as contas para cada tipo de transação de vendas, como contas a receber, cheques recebidos, e variações cambiais.

**Status**: (Sim/Não)

**Justificativa**: (caso não, justificar)

### 5.02) Compras
**Descrição**: Esta seção trata das contas contábeis usadas para registrar as transações de compras. A configuração correta destas contas garante a precisão na contabilização dos custos de aquisição de mercadorias e serviços.

**Caminho no SAP**: Para configurar as contas contábeis de compras:
1. Acesse o menu "Administração" > "Configuração Financeira".
2. Selecione "Determinação de Contas Contábeis" e, em seguida, "Compras".
3. Configure as contas para cada tipo de transação de compras, como contas a pagar, descontos obtidos, e variações cambiais.

**Status**: (Sim/Não)

**Justificativa**: (caso não, justificar)

### 5.03) Geral
**Descrição**: Nesta seção, são definidas as contas contábeis gerais que abrangem diversas operações financeiras que não se encaixam especificamente nas categorias de vendas ou compras, como taxas de depósito de cartão de crédito e ajustes de reconciliação.

**Caminho no SAP**: Para configurar as contas contábeis gerais:
1. Acesse o menu "Administração" > "Configuração Financeira".
2. Selecione "Determinação de Contas Contábeis" e, em seguida, "Geral".
3. Configure as contas gerais, como taxas de depósito de cartão de crédito, arredondamento por diferenças de moeda, e saldos iniciais.

**Status**: (Sim/Não)

**Justificativa**: (caso não, justificar)

### 5.04) Estoque
**Descrição**: A configuração das contas contábeis de estoque é crucial para o gerenciamento preciso do inventário e dos custos de mercadorias vendidas. Isso inclui a definição de contas para mercadorias para revenda, ajustes de inventário, e variações de custo médio.

**Caminho no SAP**: Para configurar as contas contábeis de estoque:
1. Acesse o menu "Administração" > "Configuração Financeira".
2. Selecione "Determinação de Contas Contábeis" e, em seguida, "Estoque".
3. Configure as contas para cada aspecto do gerenciamento de estoque, como mercadorias para revenda, variação do custo médio, e ajustes de inventário.

**Status**: (Sim/Não)

**Justificativa**: (caso não, justificar)

## 6) Definir Centros de Custo

### 6.01) Definir as Dimensões dos Centros de Custo
**Descrição**: Um centro de custo é uma unidade dentro da empresa responsável por uma função específica, como a fabricação de produtos ou fornecimento de serviços. A definição das dimensões dos centros de custo permite que as despesas e receitas sejam consolidadas para cada unidade organizacional.

**Caminho no SAP**: Para definir as dimensões dos centros de custo:
1. Acesse o menu "Administração" > "Configuração Financeira".
2. Selecione "Centros de Custo" e, em seguida, "Dimensões".
3. Defina as dimensões de centros de custo, como departamento, produto, ou projeto.

**Status**: (Sim/Não)

**Justificativa**: (caso não, justificar)

### 6.02) Definir os Centros de Custo
**Descrição**: Nesta etapa, são definidos os centros de custo específicos, que representam diferentes divisões ou departamentos dentro da empresa. Isso permite o rastreamento detalhado de receitas e despesas associadas a cada centro de custo.

**Caminho no SAP**: Para definir os centros de custo:
1. Acesse o menu "Administração" > "Configuração Financeira".
2. Selecione "Centros de Custo" e, em seguida, "Definir Centros de Custo".
3. Crie e configure os centros de custo, associando cada um às dimensões definidas anteriormente.

**Status**: (Sim/Não)

**Justificativa**: (caso não, justificar)

## 7) Definição de Despesas

### 7.01) Despesas de Importação
**Descrição**: Esta configuração é utilizada para processar os custos de importação de mercadorias ou serviços provenientes do exterior. Os custos de importação são distribuídos entre os itens recebidos e registrados no sistema.

**Caminho no SAP**: Para configurar as despesas de importação:
1. Acesse o menu "Administração" > "Configuração Financeira".
2. Selecione "Despesas" e, em seguida, "Despesas de Importação".
3. Configure as contas e alocações para despesas de importação.

**Status**: (Sim/Não)

**Justificativa**: (caso não, justificar)

### 7.02) Despesas Adicionais
**Descrição**: Definição de despesas adicionais que refletem custos extras relacionados a vendas ou compras, como taxas de entrega e serviços adicionais. Estas despesas são registradas para permitir uma contabilidade mais precisa.

**Caminho no SAP**: Para configurar as despesas adicionais:
1. Acesse o menu "Administração" > "Configuração Financeira".
2. Selecione "Despesas" e, em seguida, "Despesas Adicionais".
3. Configure as despesas adicionais e suas respectivas contas contábeis.

**Status**: (Sim/Não)

**Justificativa**: (caso não, justificar)

## 8) Definir Depósitos

### 8.01) Defina os Depósitos
**Descrição**: Nesta seção, são definidos os depósitos da empresa, que correspondem a locais físicos ou virtuais onde o estoque é armazenado. Cada depósito pode ter sua própria configuração contábil, essencial para a correta determinação do custo dos itens.

**Caminho no SAP**: Para definir os depósitos:
1. Acesse o menu "Administração" > "Configuração de Estoque".
2. Selecione "Depósitos" e, em seguida, "Definir Depósitos".
3. Configure os depósitos da empresa, especificando o código, nome, e propriedades de cada depósito.

**Status**: (Sim/Não)

**Justificativa**: (caso não, justificar)

## 9) Definir grupos de item

### 9.01) Defina os grupos de item
**Descrição**: Os grupos de item no SAP são utilizados para categorizar produtos e serviços com características semelhantes. Isso facilita o gerenciamento e a análise de estoque, vendas, e compras, permitindo a criação de relatórios mais detalhados e organizados.

**Caminho no SAP**: Para definir os grupos de item:
1. Acesse o menu "Administração" > "Configuração de Estoque".
2. Selecione "Grupos de Itens" e, em seguida, "Definir Grupos de Itens".
3. Configure os grupos de itens, especificando as categorias, métodos de planejamento, e outros parâmetros necessários para o controle de estoque e relatórios.

**Status**: (Sim/Não)

**Justificativa**: (caso não, justificar)

## 10) Impostos

### 10.01) Configuração de Imposto Retido na Fonte - IRF
**Descrição**: A configuração de Imposto Retido na Fonte (IRF) é essencial para o cumprimento das obrigações fiscais da empresa. Nesta seção, são definidos os códigos de imposto, taxas, e contas contábeis associadas a cada tipo de imposto retido.

**Caminho no SAP**: Para configurar o IRF:
1. Acesse o menu "Administração" > "Configuração Financeira".
2. Selecione "Impostos" e, em seguida, "Configuração de Impostos Retidos".
3. Configure os impostos retidos na fonte, especificando as taxas aplicáveis, códigos oficiais, e contas contábeis associadas.

**Status**: (Sim/Não)

**Justificativa**: (caso não, justificar)

### 10.02) Definir Códigos de imposto
**Descrição**: Nesta etapa, os códigos de imposto que a empresa utiliza para suas operações são definidos. Isso inclui impostos sobre vendas, serviços, e outras operações comerciais que devem ser monitoradas e reportadas.

**Caminho no SAP**: Para definir os códigos de imposto:
1. Acesse o menu "Administração" > "Configuração Financeira".
2. Selecione "Impostos" e, em seguida, "Códigos de Imposto".
3. Configure os códigos de imposto necessários, associando cada código às respectivas contas contábeis e tipos de transações.

**Status**: (Sim/Não)

**Justificativa**: (caso não, justificar)

## 11) Definir condições de pagamento

### 11.01) Lista de códigos de condição
**Descrição**: As condições de pagamento especificam os termos pelos quais os clientes e fornecedores realizam transações financeiras com a empresa. Essas condições incluem prazos, descontos por pagamento antecipado, e métodos de pagamento.

**Caminho no SAP**: Para definir as condições de pagamento:
1. Acesse o menu "Administração" > "Configuração Financeira".
2. Selecione "Condições de Pagamento" e, em seguida, "Definir Condições de Pagamento".
3. Configure as condições de pagamento, especificando os termos, prazos, e códigos de condição para cada tipo de transação.

**Status**: (Sim/Não)

**Justificativa**: (caso não, justificar)

## 12) Definir informações de cartões

### 12.01) Detalhes dos cartões
**Descrição**: Nesta seção, são cadastrados os detalhes dos cartões de crédito e débito que a empresa aceita para pagamentos ou utiliza para transações com fornecedores. Isso permite a automação de recebimentos e pagamentos por meio de cartões no SAP.

**Caminho no SAP**: Para configurar os detalhes dos cartões:
1. Acesse o menu "Administração" > "Configuração Financeira".
2. Selecione "Cartões" e, em seguida, "Detalhes dos Cartões".
3. Configure as informações dos cartões aceitos, incluindo o nome do cartão, tipo, conta contábil associada, e outros detalhes relevantes.

**Status**: (Sim/Não)

**Justificativa**: (caso não, justificar)

### 12.02) Definir informações de cartão para contas a receber (cliente)
**Descrição**: Esta configuração permite que a empresa defina como os pagamentos com cartão de crédito serão processados para as contas a receber. Isso inclui a configuração de recebimentos e a forma como os comprovantes de cartão são gerenciados.

**Caminho no SAP**: Para configurar as informações de cartão para contas a receber:
1. Acesse o menu "Administração" > "Configuração Financeira".
2. Selecione "Cartões" e, em seguida, "Configuração de Recebimento com Cartão".
3. Configure as opções de recebimento com cartão de crédito, incluindo os prazos de recebimento e os métodos de pagamento.

**Status**: (Sim/Não)

**Justificativa**: (caso não, justificar)

## 13) Definir usuários e senhas

### 13.01) Usuários
**Descrição**: Nesta seção, são definidos os usuários que terão acesso ao sistema SAP e as respectivas permissões de cada um. Isso inclui a criação de usuários, definição de senhas, e configuração de permissões de acesso baseadas em funções específicas dentro da empresa.

**Caminho no SAP**: Para definir os usuários e senhas:
1. Acesse o menu "Administração" > "Configuração Geral".
2. Selecione "Usuários" e, em seguida, "Gerenciamento de Usuários".
3. Crie novos usuários, defina suas permissões, e configure as senhas de acesso ao sistema.

**Status**: (Sim/Não)

**Justificativa**: (caso não, justificar)

## 14) Definir territórios, grupos de comissão, vendedores e estágios (níveis) de vendas

### 14.01) Se o seu negócio utiliza territórios para gerenciar seus vendedores, complete a tabela abaixo
**Descrição**: A definição de territórios permite que a empresa organize e gerencie suas equipes de vendas com base em áreas geográficas ou segmentos de mercado. Isso facilita a alocação de recursos e o monitoramento de desempenho por região.

**Caminho no SAP**: Para definir os territórios:
1. Acesse o menu "Administração" > "Configuração de Vendas".
2. Selecione "Territórios" e, em seguida, "Definir Territórios".
3. Configure os territórios, especificando as regiões ou segmentos e associando-os aos vendedores.

**Status**:(Sim/Não)

**Justificativa**: (caso não, justificar)

### 14.02) Se o seu negócio utiliza um percentual de comissão direto por vendedor, grupo de itens ou cliente, complete a tabela abaixo
**Descrição**: Esta seção permite configurar os percentuais de comissão que serão aplicados diretamente a vendedores, grupos de itens ou clientes. Isso é essencial para a automação do cálculo de comissões dentro do SAP, garantindo que as políticas de remuneração sejam seguidas corretamente.

**Caminho no SAP**: Para definir as comissões:
1. Acesse o menu "Administração" > "Configuração de Vendas".
2. Selecione "Comissões" e, em seguida, "Definir Percentuais de Comissão".
3. Configure os percentuais de comissão para cada vendedor, grupo de itens ou cliente conforme as políticas da empresa.

**Status**: (Sim/Não)

**Justificativa**: (caso não, justificar)

### 14.03) Se o seu negócio controla as vendas por vendedor, complete a tabela abaixo
**Descrição**: Esta configuração permite que as vendas sejam atribuídas e monitoradas por vendedor, facilitando a análise de desempenho individual e a aplicação de políticas de comissionamento baseadas em resultados específicos.

**Caminho no SAP**: Para configurar o controle de vendas por vendedor:
1. Acesse o menu "Administração" > "Configuração de Vendas".
2. Selecione "Vendedores" e, em seguida, "Definir Controle de Vendas".
3. Configure o controle de vendas, associando cada vendedor às suas respectivas contas e clientes.

**Status**: (Sim/Não)

**Justificativa**: (caso não, justificar)

### 14.04) Definir os Estágios (Níveis) de vendas - Oportunidades de Vendas
**Descrição**: Antes de registrar novas oportunidades de vendas, é necessário definir os estágios ou níveis de vendas, como telefonema inicial, reunião, proposta, e fechamento. Estes estágios ajudam a acompanhar o progresso das oportunidades e a aplicar metodologias de vendas estruturadas.

**Caminho no SAP**: Para definir os estágios de vendas:
1. Acesse o menu "Administração" > "Configuração de Vendas".
2. Selecione "Oportunidades de Vendas" e, em seguida, "Definir Estágios de Vendas".
3. Configure os diferentes estágios de vendas, atribuindo uma porcentagem de probabilidade de fechamento a cada estágio.

**Status**: (Sim/Não)

**Justificativa**: (caso não, justificar)

## 15) Definir grupos de clientes

### 15.01) Defina os grupos de clientes
**Descrição**: Os grupos de clientes são usados para categorizar os clientes em segmentos com características semelhantes, como tamanho da empresa, setor de atuação, ou localização geográfica. Isso facilita o gerenciamento de campanhas de marketing, políticas de preços, e análises de vendas.

**Caminho no SAP**: Para definir os grupos de clientes:
1. Acesse o menu "Administração" > "Configuração de Vendas".
2. Selecione "Grupos de Clientes" e, em seguida, "Definir Grupos de Clientes".
3. Configure os grupos de clientes, especificando as características que definem cada grupo.

**Status**: (Sim/Não)

**Justificativa**: (caso não, justificar)

## 16) Definir grupos de fornecedores

### 16.01) Defina os grupos de fornecedores
**Descrição**: Esta seção permite agrupar fornecedores em categorias com base em critérios como tipo de produto fornecido, localização, ou importância estratégica. Isso ajuda a organizar as compras e a aplicar políticas diferenciadas para cada grupo.

**Caminho no SAP**: Para definir os grupos de fornecedores:
1. Acesse o menu "Administração" > "Configuração de Compras".
2. Selecione "Grupos de Fornecedores" e, em seguida, "Definir Grupos de Fornecedores".
3. Configure os grupos de fornecedores, categorizando-os de acordo com os critérios definidos pela empresa.

**Status**: (Sim/Não)

**Justificativa**: (caso não, justificar)

## 17) Definir tipos de expedição

### 17.01) Defina os tipos de expedição
**Descrição**: Os tipos de expedição referem-se às diferentes formas de entrega de mercadorias que a empresa utiliza. Definir corretamente esses tipos no SAP facilita o gerenciamento de remessas e a aplicação de regras de frete e entrega.

**Caminho no SAP**: Para definir os tipos de expedição:
1. Acesse o menu "Administração" > "Configuração de Vendas".
2. Selecione "Expedição" e, em seguida, "Definir Tipos de Expedição".
3. Configure os tipos de expedição, especificando o nome, o método de entrega, e quaisquer outras informações relevantes.

**Status**: (Sim/Não)

**Justificativa**: (caso não, justificar)

## 18) Definir configurações iniciais de documento para todo o sistema

Esta seção abrange a configuração das opções gerais que se aplicam a todos os documentos gerados pelo sistema SAP, como o cálculo de lucro bruto, o método de arredondamento, e as políticas de bloqueio de estoque negativo.

**Caminho no SAP**: Para definir as configurações gerais de documento:
1. Acesse o menu "Administração" > "Configuração de Documentos".
2. Selecione "Configurações Gerais de Documentos".
3. Configure as opções de documento conforme as políticas da empresa, como o método de cálculo de lucro bruto, observações de arredondamento, e controle de estoque.

**Status**: (Sim/Não)

**Justificativa**: (caso não, justificar)


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
