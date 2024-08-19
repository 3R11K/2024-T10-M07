
Sumário

* [1. Introdução](#1-introdução)
    * [1.1 Matriz de Risco](#11-matriz-de-risco)
    * [1.2 Pesquisa Exploratória](#12-pesquisa-exploratória)
    * [1.3 Pesquisa Desk](#13-pesquisa-desk)
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

# 1. Entendimento de Negócios 

## 1.1 Matriz de Risco

### Introdução:

<div align="center">
<sub>Figura 1 - Matriz de risco</sub>
<img src="./imagens/matriz_de_risco.png" width="100%" >
<sup>Fonte: Material produzido pelos autores (2024)</sup>
</div>

### Descrição da Matriz:


### Plano de Ação:

&emsp;A sub-seção de Plano de Ação pretende analisar os riscos descritos na seção Matriz de Risco e, a partir disso, estabelecer estratégias para mitigar o acontecimento dos riscos mapeados. Segue a metodologia estabelecida pela equipe:

1. **Erros de Documentação** 
   - Mitigação: Implementar uma revisão duplamente reforçada para garantir que nada seja negligenciado, prevenindo erros. Dessa forma, cada task terá um responsável por executá-la e um responsável por revisá-la.

   Para exemplificar, segue o refinamento realizado na Sprint 1 (sugeito a mudanças nas demais sprints), note os campos de "Feito por" e "Revisado Por", que simboliza o responsável por realizar e revisar cada tarefa:

    <div align="center">
    <sub>Figura 2 - Exemplo de parte do Refinamento Criado pela Equipe</sub>
    <img src="./imagens/exemplo_refinamento.png" width="100%" >
    <sup>Fonte: Material produzido pelos autores (2024)</sup>
    </div>

2. **Atraso em Pequenas Entregas do Grupo**
   - Mitigação: O *Scrum Master* e *Product Owner* será responsável verificando se as entregas estão acontecendo dentro do prazo e garantindo que as entregas sejam feitas no prazo a cada Sprint.

3. **Confusão Inicial com Novas Ferramentas**
   - Mitigação: Determinar quais serão as ferramentas utilizadas e exigir que todos os membros do grupo estude-as para estarem alinhados e preparados para o projeto.

4. **Falta de Alinhamento com o Cliente**
   - Mitigação: Confirmar após cada reunião com o cliente que o projeto está no caminho certo e que todos estão alinhados.

5. **Daily Ineficiente**
   - Mitigação: A equipe ágil deve garantir que cada membro saia da daily com clareza sobre o que cada membro do grupo está fazendo, assegurando transparência no desenvolvimento diário.

6. **Falta de Motivação**
   - Mitigação: Se houver sinais de falta de engajamento, focar em atividades de desenvolvimento em grupo para reanimar a equipe.

7. **Distribuição Desigual de Tarefas**
   - Mitigação: Analisar e ajustar a distribuição de tarefas para garantir equilíbrio, como descrito anteriormente.

8. **Falta de Compromisso de Alguns Integrantes**
   - Mitigação: Definir prazos de entrega claros e cumprir rigorosamente conforme estabelecido na planning, comunicando impedimentos.

9. **Desentendimento entre Integrantes do Grupo** 
   - Mitigação: Promover comunicação aberta e resolver conflitos rapidamente, como mencionado anteriormente.

10. **Mudanças de Escopo ao Longo do Projeto** 
    - Mitigação: Analisar as mudanças cuidadosamente, designar quem melhor se encaixa para a tarefa e garantir que o trabalho seja concluído dentro do prazo.

## 1.2 Pesquisa Exploratória

## 1.3 Pesquisa Desk

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
