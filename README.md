# 🧪 Laboratório 04 – Visualização de Dados utilizando uma Ferramenta de BI

**Disciplina:** Laboratório de Experimentação de Software  
**Curso:** Engenharia de Software – 6º Período  
**Professor:** Wesley Dias Maciel

---

## 📌 Introdução

A visualização de dados é uma etapa essencial para transformar resultados experimentais em insights compreensíveis e acionáveis. Neste trabalho, utilizamos conceitos de **Business Intelligence (BI)** para analisar e representar dados relacionados a repositórios JavaScript hospedados no GitHub, com foco em compreender o impacto da **substituição de bibliotecas externas por funções nativas do JavaScript**.

O **dataset** baseia-se em informações coletadas de **100 repositórios mais populares de JavaScript**, analisando métricas **antes e depois** dessa alteração. Essa comparação visa identificar se há correlação entre a redução de dependências externas e melhorias em **segurança**, **popularidade** e **manutenibilidade** do código.

As análises e visualizações foram desenvolvidas em uma ferramenta de BI (Power BI), permitindo a exploração interativa dos dados e a extração de conclusões de forma visual e intuitiva.

---

## 📊 Metodologia

### 🔹 Fonte de Dados

O dataset utilizado foi construído a partir da mineração de repositórios do **GitHub**. Cada repositório foi analisado em dois momentos distintos:

- **Antes da substituição** de bibliotecas externas por funções nativas.
- **Depois da substituição**, com o código já adaptado.

As métricas coletadas incluem:

| Métrica | Descrição |
|----------|------------|
| ⭐ **Stars** | Número total de estrelas do repositório (popularidade). |
| 📦 **Dependencies** | Quantidade de dependências externas listadas em `package.json`. |
| 🧩 **Dev Dependencies** | Quantidade de dependências de desenvolvimento. |
| 🧨 **Vulnerable Dependencies** | Número de dependências identificadas com vulnerabilidades conhecidas. |
| 🔐 **CVEs** | Total de vulnerabilidades (Common Vulnerabilities and Exposures) relacionadas ao projeto. |

Os dados foram estruturados em um arquivo CSV e posteriormente importados para a ferramenta de BI.

### 🔹 Estrutura do Dataset

O dataset possui o seguinte esquema:

| Campo | Tipo | Descrição |
|-------|------|------------|
| `repo_name` | String | Nome do repositório |
| `stars` | Inteiro | Número de estrelas |
| `dependencies` | Inteiro | Dependências |
| `dev_dependencies` | Inteiro | Dependências de desenvolvimento |
| `vulnerable_dependencies` | Inteiro | Dependências vulneráveis |
| `cves` | Inteiro | Quantidade de CVEs |

---

## 🔍 Questões de Pesquisa (RQs)

### **RQ1:** A substituição de bibliotecas externas por funções nativas gera uma grande variação no número de dependências vulneráveis?

📈 **Hipótese:**  
- A substituição irá gerar uma grande variação principalmente nos repositórios maiores.

---

### **RQ2:** Há relação no número de estrelas com a vulnerabilidade presente nos repositórios mais famosos?

📈 **Hipótese:**  
- A popularidade pode se tornar maior devido ao menor número possível de vulnerabilidades e código mais estável.

---

### **RQ3:** Existe correlação entre o número de dependências externas e a quantidade de vulnerabilidades (CVEs)?

📈 **Hipótese:**  
- A correlação entre essas duas variáveis é diretamente proporcional, ou seja o número de dependências maior aumenta o número de vulnerabilidades.

---

## 🧭 Estrutura do Dashboard

O dashboard final será dividido em três seções principais:

1. **Caracterização do Dataset**  
   - Total de repositórios analisados  
   - Distribuição de estrelas (antes e depois)  
   - Distribuição de dependências  
   - Histograma de vulnerabilidades e CVEs  

2. **Comparação Antes x Depois**  
   - Gráficos lado a lado comparando métricas pré e pós-substituição.  
   - Indicadores de variação (Δ%).  

3. **Análises Específicas (RQs)**  
   - Visualizações dedicadas a cada questão de pesquisa, com legendas explicativas.  

---

## 📈 Resultados Esperados

- Redução significativa nas métricas de **vulnerabilidades** e **dependências externas**.  
- Pequena ou nenhuma perda em **popularidade** (estrelas).  
- Correlação negativa entre número de dependências e segurança (menos dependências → menos CVEs).  

---

## 💬 Discussão

Os resultados obtidos deverão evidenciar como a adoção de funções nativas do JavaScript pode contribuir para a **melhoria da segurança** e **simplificação da manutenção** de projetos open source.  
Além disso, será discutido se essas mudanças afetam de forma perceptível a **popularidade** dos repositórios na comunidade.

---

## 📎 Conclusão

Através da aplicação de técnicas de **Business Intelligence**, foi possível transformar dados técnicos de repositórios em **insights visuais**, auxiliando na compreensão do impacto de decisões arquiteturais no ecossistema JavaScript.  
Os dashboards criados permitem **monitorar, comparar e explorar** métricas de segurança e popularidade com clareza e objetividade.

---

## 📚 Ferramentas Utilizadas

- **Linguagem de coleta:** Python  
- **Fonte dos dados:** GitHub API  
- **Tratamento dos dados:** Pandas  
- **Visualização:** Power BI
- **Formato do dataset:** CSV  


---

> **Autores:**  
> Luiz Felipe Campos de Morais  
> Marcus Vinícius Carvalho de Oliveira  
