# 🧠 Classification Neural Network (TensorFlow.js)

Este projeto é uma implementação simples de uma **Rede Neural de Classificação** utilizando **TensorFlow.js com Node.js**.

O objetivo é demonstrar, de forma prática, como podemos treinar um modelo de Machine Learning para classificar usuários em diferentes categorias com base em características como:

* Idade (normalizada)
* Preferência de cor
* Localização

---

## 🚀 Tecnologias Utilizadas

* Node.js
* TensorFlow.js (`@tensorflow/tfjs-node`)

---

## 📊 Estrutura do Modelo

A rede neural foi construída com:

* **Camada de Entrada:** 7 features

  * Idade normalizada
  * 3 cores (One-Hot Encoding)
  * 3 localizações (One-Hot Encoding)

* **Camada Oculta:**

  * 80 neurônios
  * Função de ativação: ReLU

* **Camada de Saída:**

  * 3 neurônios
  * Categorias:

    * Premium
    * Medium
    * Basic
  * Função de ativação: Softmax

---

## 🏋️ Treinamento

O modelo é treinado utilizando:

* **Optimizer:** Adam
* **Loss Function:** Categorical Crossentropy
* **Epochs:** 100
* **Shuffle:** true

As saídas são codificadas utilizando **One-Hot Encoding**:

| Categoria | Representação |
| --------- | ------------- |
| Premium   | [1, 0, 0]     |
| Medium    | [0, 1, 0]     |
| Basic     | [0, 0, 1]     |

---

## 🔮 Predição

Após o treinamento, o modelo é capaz de prever a probabilidade de um novo usuário pertencer a cada uma das categorias.

Exemplo de saída:

```
Premium (72.31%)
Medium (20.15%)
Basic (7.54%)
```

---

## ▶️ Como Executar

Instale as dependências:

```bash
npm install
```

Execute o projeto:

```bash
node index.js
```

---

## 📚 Finalidade

Projeto acadêmico desenvolvido para fins de estudo sobre:

* Redes Neurais
* Classificação Multiclasse
* Normalização de Dados
* One-Hot Encoding
* TensorFlow.js em ambiente Node.js
