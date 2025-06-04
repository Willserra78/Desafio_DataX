# Análise de Churn de Clientes - TelecomX

![Python](https://img.shields.io/badge/Python-3.x-blue.svg)
![Jupyter Notebook](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)
![Pandas](https://img.shields.io/badge/Pandas-lightgreen.svg)
![Matplotlib](https://img.shields.io/badge/Matplotlib-red.svg)
![Seaborn](https://img.shields.io/badge/Seaborn-purple.svg)

---

## 📄 Sumário

Este projeto consiste em uma Análise Exploratória de Dados (EDA) aprofundada para identificar os principais fatores que contribuem para a evasão de clientes (Churn) na empresa de telecomunicações TelecomX. O objetivo é fornecer insights acionáveis que possam guiar a criação de estratégias eficazes de retenção de clientes.

---

## 🎯 Objetivo do Projeto

* **Identificar Padrões de Churn:** Compreender as características de clientes que churnam versus clientes que permanecem.
* **Analisar Relações:** Investigar a correlação entre diversas variáveis (demográficas, de serviço, financeiras) e a propensão ao Churn.
* **Gerar Insights Acionáveis:** Derivar recomendações estratégicas baseadas em dados para mitigar a taxa de evasão e melhorar a retenção de clientes na TelecomX.

---

## 📁 Estrutura do Repositório

O repositório está organizado da seguinte forma:

.
├── Desafio Data_X.ipynb              # Notebook principal contendo toda a análise EDA e o relatório final.
├── TelecomX_Data.json              # Dataset original utilizado para a análise.
├── assets/                         # Pasta contendo os gráficos e outras mídias do projeto.
│   ├── grafico_barras_churn_Contract.png   # Gráfico de Churn por Tipo de Contrato
│   └── grafico_barras_churn_InternetService.png # Gráfico de Churn por Serviço de Internet
└── README.md                       # Este arquivo.


---

## 🛠️ Tecnologias Utilizadas

* **Python** (versão 3.x)
* **Bibliotecas Python:**
    * `pandas` para manipulação e análise de dados.
    * `numpy` para operações numéricas.
    * `matplotlib` para visualização de dados estática.
    * `seaborn` para visualizações estatísticas atraentes.
* **Ambiente de Desenvolvimento:** Google Colab (ou Jupyter Notebook).

---

## ⚙️ Instalação e Configuração

Para executar este projeto localmente (em Jupyter Notebook) ou reproduzi-lo no Google Colab, siga os passos abaixo:

1.  **Clonar o Repositório:**
    ```bash
    git clone [https://github.com/willserra/Desafio_DataX.git](https://github.com/willserra/Desafio_DataX.git)
    cd Desafio_DataX
    ```

2.  **Criar Ambiente Virtual (Recomendado - para uso local):**
    ```bash
    python -m venv venv
    source venv/bin/activate  # No Windows: .\venv\Scripts\activate
    ```

3.  **Instalar Dependências:**
    ```bash
    pip install pandas numpy matplotlib seaborn
    ```

---

## 🚀 Como Executar a Análise

### No Google Colab:

1.  **Upload do Arquivo:** Faça o upload do arquivo `TelecomX_Data.json` para o ambiente do Google Colab (na sessão de arquivos, clique no ícone de "Upload"). Certifique-se de que ele esteja na pasta `/content/`.
2.  **Abrir o Notebook:** Abra o arquivo `Desafio Data_X.ipynb` no Google Colab.
3.  **Executar as Células:** Execute todas as células do notebook sequencialmente. O notebook está estruturado para realizar o pré-processamento, as análises e gerar os gráficos e o relatório final.

### No Jupyter Notebook (Localmente):

1.  **Certifique-se de que os arquivos `Desafio Data_X.ipynb` e `TelecomX_Data.json` estão no mesmo diretório.**
2.  **Abrir Jupyter:** Inicie o Jupyter Notebook ou JupyterLab a partir do terminal no diretório do projeto:
    ```bash
    jupyter notebook
    ```
3.  **Abrir o Notebook:** No navegador, clique em `Desafio Data_X.ipynb` para abri-lo.
4.  **Executar as Células:** Execute todas as células do notebook em ordem para reproduzir a análise completa.

---

## 📊 Insights Principais (Resumo)

A análise revelou que o Churn na TelecomX é influenciado por múltiplos fatores, com destaque para:

* **Contrato e Tempo de Serviço (`tenure`):** Clientes com contratos **mensais** e com **pouco tempo de serviço** são os mais propensos à evasão. Contratos de longo prazo demonstram ser o fator de retenção mais robusto.
* **Serviço de Internet:** A **Fibra Ótica** apresenta uma taxa de Churn significativamente maior, indicando possíveis problemas de qualidade, expectativa ou suporte neste tipo de serviço.
* **Serviços Adicionais:** A **ausência de serviços de valor agregado**, como `OnlineSecurity`, `OnlineBackup`, `DeviceProtection` e, crucialmente, **Suporte Técnico (`TechSupport`)**, está fortemente correlacionada com maior evasão. Esses serviços atuam como "fatores de aderência".
* **Método de Pagamento:** O **Cheque Eletrônico** é um método de pagamento associado a uma alta taxa de Churn.
* **Perfis Demográficos:** Clientes **idosos**, **sem parceiro** e **sem dependentes** demonstram maior propensão a churnar.

---

## 🖼️ Gráficos Principais

Para ilustrar os insights mais impactantes, destacamos alguns dos gráficos gerados na análise:

### Proporção de Churn por Tipo de Contrato
*(Este gráfico demonstra claramente como clientes com contratos mensais têm uma taxa de Churn dramaticamente maior.)*
![Churn por Tipo de Contrato](assets/grafico_barras_churn_Contract.png)

### Proporção de Churn por Serviço de Internet
*(Este gráfico evidencia a alta taxa de Churn entre clientes com serviço de Fibra Ótica, um ponto crítico de atenção.)*
![Churn por Serviço de Internet](assets/grafico_barras_churn_InternetService.png)

**Para visualizar *todos* os gráficos detalhados e a análise completa, acesse o notebook `Desafio Data_X.ipynb` diretamente no seu repositório GitHub.** O GitHub possui um renderizador de notebooks que exibirá todos os gráficos e o relatório de forma interativa.

---

## 💡 Recomendações Estratégicas (Resumo)

Com base nos insights, algumas recomendações para a TelecomX incluem:

* **Programas de Fidelização Acelerada:** Focar em clientes novos e de contrato mensal com check-ins proativos e ofertas de migração para contratos mais longos.
* **Otimização da Fibra Ótica:** Investigar profundamente a experiência do cliente com fibra (qualidade, suporte, expectativas) e realizar ajustes.
* **Valorização de Serviços Agregados:** Integrar serviços como Suporte Técnico em pacotes base ou oferecer test-drives para aumentar a percepção de valor e "aderência".
* **Incentivos para Migração de Pagamento:** Oferecer bônus ou descontos para clientes que migram do Cheque Eletrônico para métodos de pagamento automáticos.
* **Atendimento Personalizado:** Desenvolver abordagens e ofertas segmentadas para clientes idosos e para indivíduos sem parceiro/dependentes.

Para o detalhamento completo das recomendações e suas justificativas, consulte a seção "Recomendações Estratégicas para Retenção" no notebook `Desafio Data_X.ipynb`.

---

## 📝 Resultados e Output

O resultado final deste projeto é um notebook Jupyter (`Desafio Data_X.ipynb`) que serve como um relatório técnico completo. Ele contém:

* O código Python para todas as etapas de pré-processamento e análise.
* Gráficos visualmente claros (box plots, gráficos de barras, heatmap de correlação) que ilustram os padrões encontrados.
* Texto explicativo detalhado para cada seção da análise.
* Uma seção consolidada de "Principais Insights e Descobertas".
* Um conjunto de "Recomendações Estratégicas para Retenção" baseadas em dados.

---

## 📞 Contato

Em caso de dúvidas ou para mais informações, sinta-se à vontade para entrar em contato:

* **Seu Nome:** William S. Serra.
* **LinkedIn:** [LinkedIn](https://www.linkedin.com/in/william-serra)
* **Email:** [e-mail](mailto:w.serra1978@gmail.com)
