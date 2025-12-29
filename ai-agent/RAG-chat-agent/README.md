# RAG Chat Agent: Converse com seus Documentos

Este fluxo do **n8n** implementa um sistema completo de **RAG (Retrieval-Augmented Generation)**. Ele permite que você faça upload de documentos no **Google Drive** e converse com eles através de um bot no **Telegram**.

## 📝 Descrição

O sistema monitora uma pasta específica no Google Drive. Assim que um novo arquivo (PDF, TXT, etc.) é adicionado ou atualizado, ele é automaticamente processado, vetorizado e armazenado no **Pinecone**. Quando você faz uma pergunta no Telegram, o agente utiliza IA para buscar as informações mais relevantes nos seus documentos e gerar uma resposta precisa.

## 🚀 Funcionalidades

- **Ingestão Automática**: Monitora o Google Drive e processa novos arquivos automaticamente.
- **Busca Semântica (RAG)**: Encontra trechos relevantes nos documentos mesmo que não usem as palavras exatas.
- **Interface via Telegram**: Converse com sua base de conhecimento de forma simples e móvel.
- **Alta Performance**:
  - **Embeddings**: Google Gemini (rápido e eficiente).
  - **LLM**: Groq (latência extremamente baixa).
  - **Vector DB**: Pinecone.

## 🎥 Demonstração

![Execução do RAG](3.execution.gif)

## 🛠️ Como Funciona o Fluxo

O projeto é dividido em duas partes principais:

### 1. Pipeline de Ingestão (Indexação)
1. **Google Drive Trigger**: Detecta novos arquivos ou atualizações na pasta monitorada.
2. **Download File**: Baixa o conteúdo do arquivo.
3. **Text Splitter**: Divide o texto em pedaços menores (chunks) para melhor processamento.
4. **Embeddings (Gemini)**: Converte o texto em vetores numéricos.
5. **Pinecone Store**: Salva os vetores no banco de dados para busca futura.

### 2. Pipeline de Chat (Consulta)
1. **Telegram Trigger**: Recebe a pergunta do usuário.
2. **AI Agent**: Analisa a intenção e decide consultar a base de conhecimento.
3. **Vector Store Tool**: Busca os trechos mais relevantes no Pinecone usando a mesma técnica de embeddings.
4. **LLM (Groq)**: Gera uma resposta natural baseada nos documentos encontrados.
5. **Send Message**: Envia a resposta final para o Telegram.

## 📋 Pré-requisitos

Para utilizar este fluxo, você precisará das seguintes credenciais no n8n:

- **Google Drive API** (OAuth2).
- **Pinecone API** (Vector Database).
- **Google Gemini API** (Para embeddings).
- **Groq API** (Para geração de texto/chat).
- **Telegram API** (Para o bot).
