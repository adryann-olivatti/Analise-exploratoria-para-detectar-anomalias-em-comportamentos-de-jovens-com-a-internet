# 📊 Análise Exploratória: Impactos das Redes Sociais na Saúde Mental dos Adolescentes

[![Python](https://img.shields.io/badge/Python-3.8%2B-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Pandas](https://img.shields.io/badge/Pandas-Data_Analysis-150458?style=for-the-badge&logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![Seaborn](https://img.shields.io/badge/Seaborn-Data_Visualization-3776AB?style=for-the-badge)](https://seaborn.pydata.org/)
[![Google Colab](https://img.shields.io/badge/Google_Colab-Jupyter_Notebook-F9AB00?style=for-the-badge&logo=googlecolab&logoColor=white)](https://colab.research.google.com/)

---

## 👥 Autores & Contexto

> [!NOTE]
> **Trabalho Prático** desenvolvido para a disciplina de **Fundamentos de Ciência de Dados**.
> * **Henrique Chiabai da Silva**
> * **Adryann Henrique Oliveira Olivatti**

---

## 🎯 Objetivo do Projeto

Analisar a relação entre o comportamento digital (uso de redes sociais e tempo de tela), estilo de vida (sono e exercícios) e os níveis de estresse, ansiedade e depressão em adolescentes.

* **Dataset:** [Teenager Mental Health Dataset (Kaggle)](https://www.kaggle.com/datasets/itszubi/impact-of-social-media-on-teens-mental-health)
* **Amostra:** 1.200 registros de jovens entre 13 e 19 anos (0% de dados nulos).

---

## 🛠️ Engenharia de Dados (Feature Engineering)

Para enriquecer a análise, foi criada a variável categórica derivativa:
* **`physical_activity_label`**: Classifica se o jovem atinge a recomendação da OMS de pelo menos **30 minutos diários** (0.5h) de exercícios físicos (`Sim` / `Não`).

---

## 🔍 Perguntas de Pesquisa e Principais Achados

| # | Pergunta Investigada | Técnica Visual | Resultado / Achado |
| :-: | :--- | :-: | :--- |
| **1** | **Redes sociais causam estresse/ansiedade?** | `sns.regplot` | ⚪ **Sem relação direta:** A linha de tendência é neutra. Horas brutas de tela não indicam variação direta de estresse. |
| **2** | **Como a depressão afeta estresse e ansiedade?** | `sns.kdeplot` | 🔴 **Forte sobreposição:** Adolescentes com depressão concentram-se no patamar mais elevado de ansiedade e estresse simultâneos. |
| **3** | **Jovens com depressão usam mais redes sociais?** | `sns.boxplot` | 📈 **Sim:** A mediana de horas diárias em redes sociais do grupo com depressão é significativamente maior e mais compacta no topo. |
| **4** | **Interação social presencial reduz o vício digital?** | `sns.barplot` | ⚖️ **Sem impacto:** Níveis médios de vício permanecem praticamente equivalentes independente da interação social. |
| **5** | **Adolescentes com depressão dormem menos?** | `sns.violinplot` | 📉 **Sim:** A distribuição de horas de sono do grupo com indicativo depressivo é achatada e deslocada para baixo. |
| **6** | **Atividade física diária reduz estresse e ansiedade?** | `sns.boxplot` | ❓ **Resultado Inesperado:** Não foi observada alteração estatística expressiva entre quem pratica ou não o tempo mínimo de exercícios. |

---

## 💡 Principais Conclusões

> [!IMPORTANT]
> * **Tempo de Tela vs. Saúde Mental:** O tempo bruto gasto em redes sociais isoladamente não explica quadros de estresse ou ansiedade, sugerindo que o **padrão de uso e conteúdo** consumido podem ter peso maior do que as horas nominais.
> * **Perfil de Risco:** Quadros depressivos aparecem fortemente correlacionados ao efeito combinado de **alto estresse, alta ansiedade, privação de sono e elevado tempo em redes sociais**.
> * **Aplicação de IA:** Os dados e correlações mapeadas nesta análise exploratória servem de base para o treinamento de modelos de **Machine Learning** voltados à identificação e triagem precoce de riscos psicológicos em jovens.
