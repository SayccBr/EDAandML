# Análise Demográfica e Predição de Evasão no IF Goiano  
**Machine Learning para Retenção e Excelência Acadêmica**

![Python](https://img.shields.io/badge/Python-3.10%2B-blue?logo=python)
![Pandas](https://img.shields.io/badge/Pandas-2.0%2B-green?logo=pandas)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-1.3%2B-orange?logo=scikitlearn)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-purple?logo=jupyter)

---

Este repositório apresenta uma **análise completa** de dados do **IF Goiano – Campus Iporá**, com:

- **Análise Exploratória (EDA)**
- **Modelos de Machine Learning**
- **Predição de evasão e alto desempenho (IRA ≥ 7.5)**

---
## Objetivos do Projeto

### 1. **Perfil dos Estudantes**
- Etnia/Raça  
- Sexo  
- Zona residencial  
- Forma de ingresso e cotas  
- Curso/Área  
- Distribuição do IRA  

### 2. **Previsão com ML**
| Alvo | Modelo |
|------|--------|
| **Evasão** | Random Forest |
| **IRA Alto (≥7.5)** | Random Forest |

---

## Limpeza e Pré-processamento

- Remoção de colunas irrelevantes
- Tratamento de valores inválidos: `'-'`, `'NAN'`, `'None'`, `'.'`
- Conversão do **IRA** (vírgula → ponto)
- Criação de variáveis:
  - `Evasao` (1 = evadido)
  - `IRA_alto` (1 = ≥7.5)
  - `Cota` (1 = cotista)
- **Agrupamento de cursos**:
  - `Sistemas`, `Redes`, `TI` → **Informática**
- **Codificação**: `LabelEncoder`

---

## Destaques da Análise Demográfica

| Métrica | Valor |
|--------|-------|
| **Registros limpos** | **6.255** |
| **Cotistas** | 471 (7.5%) |
| **Não cotistas** | 5.784 (92.5%) |
| **Evadidos** | 1.334 (21.3%) |
| **IRA ≥ 7.5** | 2.233 (35.7%) |

> Todos os gráficos estão em: [`results/graficos/`](./results/graficos/)

---

## Resultados dos Modelos

### Predição de **Evasão**

| Modelo | Acurácia | Precisão | Recall | F1-score |
|--------|----------|----------|--------|----------|
| Regressão Logística | 0.714 | 0.404 | 0.715 | 0.516 |
| **Random Forest** | **0.717** | **0.411** | **0.757** | **0.533** |

**Features mais importantes (Evasão):**
1. **IRA** – `0.7232`  
2. **Curso** – `0.1215`  
3. **Forma de Ingresso** – `0.0837`  
4. **Etnia** – `0.0305`  
5. **Sexo** – `0.0195`

---

### Predição de **IRA Alto (≥7.5)**

| Modelo | Acurácia | Precisão | Recall | F1-score |
|--------|----------|----------|--------|----------|
| Regressão Logística | 0.551 | 0.409 | 0.575 | 0.478 |
| **Random Forest** | **0.675** | **0.536** | **0.682** | **0.600** |

> Matrizes e importância: [`results/matrizes_confusao/`](./results/matrizes_confusao/), [`results/importancia_features/`](./results/importancia_features/)

---

## Tecnologias
Linguagem: Python 3.10+
Bibliotecas:
  - pandas
  - numpy
  - matplotlib
  - seaborn
  - scikit-learn
  - jupyter

Como Executar
bash# 1. Clone o repositório
git clone https://github.com/SayccBr/EDAandML.git
cd EDAandML

# 2. Crie ambiente virtual
python -m venv venv
source venv/bin/activate      # Linux/Mac
venv\Scripts\activate         # Windows

# 3. Instale dependências
pip install -r requirements.txt

# 4. Abra no Jupyter
jupyter notebook
Execute:
eda/analise_demografica.ipynb
models/modelos_ml.ipynb


Relatório Técnico (SBC)
Formato oficial (8–12 páginas):
report/Relatorio_Tecnico.pdf

Autor
SayccBr
GitHub | IF Goiano – Campus Iporá

"Dados que salvam futuros."
text---

## PRONTO PARA USAR!

1. **Copie todo o código acima**
2. **Cole em `README.md` no seu repositório**
3. **Commit e push**
Relatório Técnico (SBC)
Formato oficial:
Relatorio_Tecnico.pdf

