# PySpark

# Análise de Transações PIX

Este projeto tem como objetivo analisar transações PIX para identificar padrões de uso e detectar possíveis fraudes, utilizando a metodologia CRISP-DM. Desenvolvido como parte do meu curso de Ciência de Dados, este repositório contém a análise completa, desde a preparação dos dados até a modelagem e avaliação.

## 🚀 Status do Projeto

✅ **Fase 1: Entendimento do Negócio** - Concluído
✅ **Fase 2: Entendimento dos Dados** - Concluído
✅ **Fase 3: Preparação dos Dados** - Concluído
✅ **Fase 4: Modelagem** - Concluído
✅ **Fase 5: Avaliação** - Concluído
⬜ **Fase 6: Implantação** - A Ser Iniciado

## 🎯 Objetivos do Projeto

Os principais objetivos deste projeto foram:

* Limpar e pré-processar os dados das transações PIX.
* Analisar padrões de uso do PIX, como canais e valores de transação mais comuns.
* Utilizar PySpark MLlib para treinar e avaliar um modelo de detecção de fraude.
* Avaliar o desempenho do modelo e propor recomendações para melhorias futuras.

## 🏦 Contexto de Negócio

Trabalho em um banco onde o PIX é o principal meio de pagamento. O banco deseja compreender o perfil dos clientes que utilizam o PIX e identificar transações fraudulentas. Além disso, há um foco em analisar as transações de um cliente específico de alto valor para o banco, compilando um relatório detalhado de suas transações dos últimos 2 anos.

## 📊 Dados

O conjunto de dados fornecido incluiu as seguintes informações para cada transação PIX:

* **Detalhes da transação**: valor, tempo, CPF/CNPJ do remetente e receptor, tipo de transação.
* **Etiqueta de fraude**: uma variável binária indicando se a transação foi fraudulenta (1) ou não (0).

## 📈 Análise Exploratória de Dados (AED) e Insights

A análise exploratória de dados revelou insights importantes sobre o cliente "Jonathan Gonsalve", que é o único cliente presente na base de dados. Observações chave incluem:

* **Alta Taxa de Transferências PIX Mensal**: O cliente Jonathan Gonsalves apresenta um volume muito elevado de transferências PIX mensalmente.
* **Categoria Predominante**: A maior categoria de transação para este cliente é a **transferência bancária**.
* **Padrão de Transação com o BTG**: O segundo banco com o qual o cliente mais transaciona é o BTG. No entanto, o valor total transacionado com o BTG é o menor, indicando que o cliente realiza **muitas transações de menor valor** para este banco.
* **Indício de Uso PJ em Conta PF**: A alta taxa de transferências com altos valores sugere que o cliente pode estar utilizando sua conta de Pessoa Física (PF) para propósitos de Pessoa Jurídica (PJ).

## 🔍 Detecção de Fraudes e Modelagem

Foi possível verificar um **alto índice de tentativas de fraude** na conta deste cliente.

* Todas as tentativas de fraude identificadas foram com **valores acima de R$19.999,00** e com a **categoria de transferência**.
* Para a detecção de fraudes, foi utilizado o modelo de **Regressão Logística** do PySpark MLlib.

### Matriz de Confusão do Modelo

A avaliação do modelo resultou na seguinte matriz de confusão:

* `0.0`: Não fraude
* `1.0`: Fraude

* **Real 0.0 (Não Fraude) / Predito 0.0 (Não Fraude)**: `233` vezes o modelo classificou corretamente como **não fraude**. (Verdadeiro Negativo)
* **Real 0.0 (Não Fraude) / Predito 1.0 (Fraude)**: `1` vez o modelo classificou como fraude, mas era **não fraude**. (Falso Positivo)
* **Real 1.0 (Fraude) / Predito 0.0 (Não Fraude)**: `0` vezes o modelo classificou como não fraude, mas era **fraude**. (Falso Negativo)
* **Real 1.0 (Fraude) / Predito 1.0 (Fraude)**: `4544` vezes o modelo classificou corretamente como **fraude**. (Verdadeiro Positivo)

**Interpretação:**
O modelo demonstrou uma excelente capacidade em identificar transações fraudulentas (4544 Verdadeiros Positivos), não deixando nenhuma fraude passar despercebida (0 Falsos Negativos). No entanto, ele apresentou um Falso Positivo (classificou como fraude uma transação que não era), o que pode gerar algum alerta desnecessário. A capacidade de identificar corretamente as transações não fraudulentas também é boa (233 Verdadeiros Negativos).

## 💡 Conclusões e Recomendações

Com base nas análises e nos resultados do modelo:

* Há uma **alta tentativa de transações com fraude** na conta do cliente Jonathan Gonsalves.
* Uma ação possível para mitigar as fraudes seria **diminuir o limite máximo de transferência de PIX do cliente**.
* Recomenda-se uma investigação mais aprofundada sobre o uso da conta, dada a suspeita de que o cliente esteja utilizando uma conta PF para propósitos de PJ devido à alta frequência e valores das transferências.
* O modelo de Regressão Logística, embora com excelente desempenho na detecção de fraudes, pode ser ajustado para reduzir os falsos positivos, minimizando alertas desnecessários.



## 🛠️ Tecnologias Utilizadas

* Python
* PySpark
* Jupyter Notebooks

## 🤝 Contribuição

Sinta-se à vontade para acompanhar o projeto. Sugestões e feedback são sempre bem-vindos!
