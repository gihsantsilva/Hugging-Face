# 🤖 RAG (Retrieval-Augmented Generation) com Hugging Face, FAISS e Python

Este projeto demonstra a construção de uma aplicação simples utilizando **RAG (Retrieved-Augmented Generation)**.
O sistema combina **embeddings** com Sentence-Transformers, **busca vetorial** com FAISS e **geração de texto** com o modelo **Llama 3.1 8B Instruct**, publicado no HuggingFace Hub.

---

## 📑 Índice

* [Descrição do Projeto](#descrição-do-projeto)
* [Pré-requisitos](#pré-requisitos)
* [Arquitetura do RAG](#arquitetura-do-rag)
* [Como Executar o Projeto](#como-executar-o-projeto)
* [Funcionalidades](#funcionalidades)
* [Estrutura do Código](#estrutura-do-código)
* [Apresentação da Tarefa](#apresentação-da-tarefa)
* [Licença](#licença)
* [Contribuidores](#contribuidores)

---

## 🧾 Descrição do Projeto

Este projeto implementa uma pipeline RAG completa contendo:

* Geração de embeddings com **Sentence-Transformers**
* Indexação e busca vetorial utilizando **FAISS**
* Consulta a uma LLM via **HuggingFace Inference API**
* Integração entre recuperação e geração para fornecer respostas contextualizadas

O objetivo principal é demonstrar como reduzir alucinações de modelos de linguagem, incorporando **contexto real recuperado de documentos**.

Ideal para quem deseja aprender os fundamentos de RAG ou criar uma base para projetos maiores de IA aplicada.

---

## ✅ Pré-requisitos

* Python 3.10 ou superior
* Conta na HuggingFace com **HF_TOKEN** válido
* Dependências do projeto:

  ```
  sentence-transformers
  faiss-cpu
  huggingface_hub
  ```

---

## 🧱 Arquitetura do RAG

A solução segue estas etapas:

1. **Indexação dos documentos**

   * Criação de embeddings usando Sentence-Transformers
   * Armazenamento no índice vetorial FAISS

2. **Recuperação (Retrieval)**

   * A pergunta é convertida para embedding
   * O FAISS retorna os trechos mais similares

3. **Geração (Generation)**

   * O contexto recuperado é enviado juntamente com a pergunta para a LLM
   * A saída é uma resposta fundamentada e com menos alucinações

---

## ▶️ Como Executar o Projeto

1. Clone o repositório:

   ```bash
   git clone https://github.com/seuusuario/nome-do-repo
   cd nome-do-repo
   ```

2. Crie e ative um ambiente virtual (opcional, mas recomendado):

   ```bash
   python -m venv venv
   source venv/bin/activate  # Linux/Mac
   venv\Scripts\activate     # Windows
   ```

3. Instale as dependências:

   ```bash
   pip install -r requirements.txt
   ```

4. Defina sua variável de ambiente com o token da HuggingFace:

   ```bash
   export HF_TOKEN=sua_chave_aqui        # Linux/Mac
   set HF_TOKEN=sua_chave_aqui           # Windows
   ```

5. Abra e execute o notebook:

   ```bash
   jupyter notebook Atividade_11_Indo_Além_(Hugging_Face).ipynb
   ```

---

## 🎯 Funcionalidades

* 🔍 Busca semântica em documentos com FAISS
* 🤖 Geração de respostas com contexto usando Llama 3.1 8B
* 📚 Sistema simples e funcional de RAG
* 📝 Loop de perguntas com impressão das respostas
* 🧪 Fácil de adaptar para PDFs, bases internas e projetos reais

---

## 📂 Estrutura do Código

O arquivo principal é o notebook:

```
Atividade_11_Indo_Além_(Hugging_Face).ipynb
```

Ele contém:

* Instalação das bibliotecas
* Criação de embeddings
* Indexação FAISS
* Função `rag()` para integração entre recuperação e geração
* Loop final de consultas

---

## 📊 Apresentação da Tarefa

O diretório também inclui a apresentação com:

* Problema das alucinações em LLMs
* Arquitetura RAG utilizada
* Resultados obtidos com o código

Essa apresentação faz parte da **Etapa 3 da atividade acadêmica**.

---

## 📝 Licença

Este projeto é de uso educacional.
Você pode utilizá-lo, estudar, modificar e expandir livremente.

---

## 🙋 Contribuidores

* **Giovanna Silva** – Desenvolvimento do código, experimentação e apresentação.
  GitHub: [https://github.com/gihsantsilva](https://github.com/gihsantsilva)
* **Enrico Genaro** – Desenvolvimento do código, experimentação e apresentação.
  GitHub: [https://github.com/enricobeiramar](https://github.com/enricobeiramar)
