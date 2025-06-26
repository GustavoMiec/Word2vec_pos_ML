# 🧠 Classificação de Artigos com Word Embeddings (CBOW & Skip-Gram)

Este projeto realiza a **classificação de categorias de artigos** utilizando **Word Embeddings** pré-treinados com os modelos **CBOW** e **Skip-Gram**. O objetivo é transformar os títulos em vetores numéricos e aplicar **Regressão Logística** para prever a categoria de cada artigo.

---

## 📂 Estrutura dos Arquivos

- `teste.csv`: Dataset com duas colunas:
  - `title`: título do artigo (texto)
  - `category`: categoria do artigo (rótulo)
- `cbow_s300.txt`: Vetores de palavras pré-treinados com o modelo CBOW (300 dimensões)
- `skip_s300.txt`: Vetores de palavras pré-treinados com o modelo Skip-Gram (300 dimensões)

---

## 📥 Download dos Word Embeddings

Para executar este projeto, é necessário baixar os arquivos de embeddings do NILC (Universidade de São Paulo):

🔗 **http://nilc.icmc.usp.br/nilc/index.php/repositorio-de-word-embeddings-do-nilc**

Baixe os seguintes arquivos:

- `cbow_s300.txt` → CBOW Word2Vec com 300 dimensões  
- `skip_s300.txt` → Skip-Gram Word2Vec com 300 dimensões

📌 Coloque esses arquivos no mesmo diretório do seu notebook/script, ou atualize os caminhos no código.

---

## 🛠️ Tecnologias e Bibliotecas

- Python 3.x
- [Pandas](https://pandas.pydata.org/)
- [NumPy](https://numpy.org/)
- [NLTK](https://www.nltk.org/)
- [Gensim](https://radimrehurek.com/gensim/)
- [Scikit-Learn](https://scikit-learn.org/)

---

## ⚙️ Etapas do Projeto

1. **Leitura dos dados de entrada**
2. **Pré-processamento e tokenização** dos títulos
3. **Geração de vetores de palavras** usando modelos CBOW e Skip-Gram
4. **Combinação dos vetores por soma**
5. **Criação da matriz de vetores** para todos os títulos
6. **Treinamento** com `LogisticRegression`
7. **Avaliação com classification_report**
8. **Comparação com DummyClassifier (baseline)**
9. **Repetição do processo usando embeddings Skip-Gram**

---

## 📊 Avaliação

A performance dos modelos é medida pelas métricas:

- **Precisão (Precision)**
- **Revocação (Recall)**
- **F1-Score**

Comparações realizadas entre:
- ✅ Modelo com CBOW  
- ✅ Modelo com Skip-Gram  
- 🔸 Classificador aleatório (DummyClassifier)

---

## ✅ Conclusões

✅ O uso de **Word Embeddings** melhora significativamente a capacidade de classificação dos títulos de artigos.  
✅ Modelos como CBOW e Skip-Gram conseguem representar semanticamente palavras semelhantes.  
🔁 O DummyClassifier serve como referência básica (baseline).

---

## 🚀 Como Executar

1. Clone este repositório
2. Instale as dependências:
```bash
pip install pandas nltk gensim scikit-learn
```

3. Baixe os arquivos `cbow_s300.txt` e `skip_s300.txt` (veja seção de download acima)
4. Execute o notebook ou script principal

---

## 👨‍💻 Autor

**Gustavo Costa**  
