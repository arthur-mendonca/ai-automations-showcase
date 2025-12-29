# 🤖 AI Automations Showcase

Bem-vindo ao meu portfólio de automações com N8N! Este repositório reúne projetos práticos que demonstram o poder da integração entre **n8n**, **LLMs** (Google Gemini, Groq) e ferramentas de produtividade (Google Workspace, Telegram, WhatsApp) para resolver problemas reais.

## 📂 Projetos em Destaque

### 1. [Agentes de IA](./ai-agent)
Uma coleção de assistentes inteligentes capazes de manter conversas, usar memória e executar ações.

- **[WhatsApp AI Bot](./ai-agent/whatsapp-bot)**: Um assistente de atendimento via WhatsApp que usa o Gemini para responder clientes de forma natural, mantendo o contexto da conversa.
- **[RAG Chat Agent](./ai-agent/RAG-chat-agent)**: Um sistema de *Retrieval-Augmented Generation* onde você conversa com seus próprios documentos (PDFs, TXTs) armazenados no Google Drive via Telegram.
- **[Personal Calendar Agent](./ai-agent/calendar-agent)**: Uma "secretária virtual" no Telegram que gerencia sua agenda no Google Calendar (cria, consulta, edita e remove eventos) através de comandos de voz ou texto.

### 2. [Gerador de Currículos Personalizados](./cv-generator)
Uma automação que acaba com o trabalho manual de adaptar currículos.
- **O que faz**: Cruza seus dados profissionais (de uma planilha) com a descrição de uma vaga enviada pelo Telegram.
- **Resultado**: Gera um documento Google Docs com um currículo reescrito pela IA, focado especificamente naquela oportunidade.

### 3. [Gerador de Questões de Medicina](./med-questoes)
Um sistema de estudo contínuo ("Gym pass" de questões) para estudantes de medicina.
- **O que faz**: Gera questões inéditas de residência médica com IA, salva em banco de dados e envia diariamente como quizzes interativos no Telegram.
- **Destaque**: Possui gabarito protegido (spoiler) para estudo ativo.

### 4. [Error Handler (Monitor de Falhas)](./error)
Um fluxo essencial para ambientes de produção.
- **O que faz**: Monitora outros fluxos no n8n. Se algo quebrar, captura o erro e envia um alerta detalhado por e-mail com link direto para o debug.

---

## 🛠️ Stack Tecnológica

- **Orquestração**: [n8n](https://n8n.io/)
- **Inteligência Artificial**: Google Gemini, Groq, Pinecone (Vector DB)
- **Integrações**: WhatsApp Business API, Telegram Bot API, Google Workspace (Sheets, Docs, Drive, Gmail, Calendar)

## 📬 Contato

Gostou das automações? Sinta-se à vontade para explorar os diretórios individuais para ver detalhes de implementação, fluxos e demonstrações.
