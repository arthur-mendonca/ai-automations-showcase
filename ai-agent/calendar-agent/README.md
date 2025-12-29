# Agente de Calendário com IA (Gemini) via n8n

Este projeto implementa um assistente pessoal inteligente no **n8n** que gerencia seu **Google Calendar** através do **Telegram**. Utilizando o modelo **Google Gemini**, o agente é capaz de compreender linguagem natural para criar, listar, atualizar e excluir eventos na sua agenda.

## 📝 Descrição

O fluxo transforma o Telegram em uma interface de comando para sua agenda. Você pode conversar com o bot como se fosse uma secretária humana, pedindo para agendar compromissos, verificar sua disponibilidade ou remarcar reuniões, tudo em português (ou outro idioma configurado).

## 🚀 Funcionalidades

- **Integração com Telegram**: Interação via chat simples e direto.
- **Inteligência Artificial (Gemini)**: Interpreta comandos complexos e contexto.
- **Gestão de Eventos**:
  - **Criar**: "Agendar almoço com cliente amanhã ao meio-dia".
  - **Consultar**: "O que tenho na minha agenda para sexta-feira?".
  - **Atualizar**: "Mudar o almoço para às 13h".
  - **Excluir**: "Cancelar a reunião de hoje".
- **Memória**: O bot mantém o contexto da conversa para facilitar ajustes e correções.

## 🎥 Demonstração

![Demonstração do Agente](2.execucao.gif)

## 🛠️ Como Funciona o Fluxo

1. **Telegram Trigger**: Captura as mensagens enviadas para o seu bot no Telegram.
2. **AI Personal Agent**: O nó central que utiliza o Gemini para decidir qual ação tomar.
3. **Ferramentas (Tools)**: O agente tem acesso a funções específicas do Google Calendar:
   - `Create an event`
   - `Get many events` (para listar)
   - `Get an event` (para buscar detalhes específicos)
   - `Update an event`
   - `Delete an event`
4. **Resposta**: O agente processa o resultado da ferramenta e envia uma resposta natural de volta via Telegram.

## 📋 Pré-requisitos

Para rodar este fluxo, você precisará configurar no n8n:

- Credenciais do **Telegram API** (Bot Father).
- Credenciais do **Google Calendar** (OAuth2).
- Credenciais da API do **Google Gemini**.
