# PySpark

# Análise de Transações PIX

Este projeto tem como objetivo analisar transações PIX para identificar padrões de uso e detectar possíveis fraudes, utilizando a metodologia CRISP-DM. Desenvolvido como parte do meu curso de Ciência de Dados, esta primeira versão foca na fase de Preparação de Dados.

## 🚀 Status do Projeto

✅ **Fase 1: Entendimento do Negócio** - Concluído
✅ **Fase 2: Entendimento dos Dados** - Em Andamento
✅ **Fase 3: Preparação dos Dados** - Concluído (parte inicial)
⬜ **Fase 4: Modelagem** - A Ser Iniciado
⬜ **Fase 5: Avaliação** - A Ser Iniciado
⬜ **Fase 6: Implantação** - A Ser Iniciado

## 🎯 Objetivos do Projeto

Os principais objetivos deste projeto são:

* Limpar e pré-processar os dados das transações PIX.
* Analisar padrões de uso do PIX, como canais e valores de transação mais comuns.
* Utilizar PySpark MLlib para treinar e avaliar um modelo de detecção de fraude.
* Avaliar o desempenho do modelo e propor recomendações para melhorias futuras.

## 🏦 Contexto de Negócio

Trabalho em um banco onde o PIX é o principal meio de pagamento. O banco deseja compreender o perfil dos clientes que utilizam o PIX e identificar transações fraudulentas. Além disso, há um foco em analisar as transações de um cliente específico de alto valor para o banco, compilando um relatório detalhado de suas transações dos últimos 2 anos.

## 📊 Dados

O conjunto de dados fornecido inclui as seguintes informações para cada transação PIX:

* **Detalhes da transação**: valor, tempo, CPF/CNPJ do remetente e receptor, tipo de transação.
* **Etiqueta de fraude**: uma variável binária indicando se a transação foi fraudulenta (1) ou não (0).

## 💡 Próximos Passos (Análise Exploratória de Dados e Engenharia de Features)

Nas próximas etapas, com os dados preparados, serão realizadas as seguintes análises utilizando PySpark:

* **Análise Exploratória de Dados (AED)**:
    * Identificação das chaves PIX mais utilizadas.
    * Análise dos valores de transação mais comuns.
    * Distribuição dos valores de transação por hora e dia.
    * Verificação dos bancos que receberam mais transferências por dia.
    * Distribuição das transações por tipo de pessoa (Pessoa Física ou Pessoa Jurídica).
* **Engenharia de Features**:
    * Criação de novas características que podem ser úteis para a detecção de fraudes, como o número de transações realizadas pelo mesmo remetente em um período específico.



## 🛠️ Tecnologias Utilizadas (Previsão)

* Python
* PySpark
* Jupyter Notebooks (ou equivalente)
* Pandas (para manipulação de dados, se necessário)

## 🤝 Contribuição

Sinta-se à vontade para acompanhar o progresso deste projeto. Sugestões e feedback são sempre bem-vindos!
