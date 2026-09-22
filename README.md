# Assistente de Investimentos com RPA e IA (n8n + Gemini)

Projeto prático desenvolvido para o desafio de RPA da DIO. A automação processa dados de clientes, gera e-mails personalizados utilizando Inteligência Artificial (Google Gemini) e realiza o disparo individualizado respeitando limites de taxa de API.

## 🛠️ Tecnologias Utilizadas
- **n8n** (Execução local via Docker)
- **Google Gemini API** (Geração do texto e e-mail via IA)
- **Gmail API / OAuth2** (Disparo automatizado de e-mails)
- **JavaScript** (Tratamento e higienização de dados em JSON)

## 🔄 Fluxo de Funcionamento
1. **Scraping e Extração**: Leitura e estruturação dos dados dos clientes.
2. **Mesclagem e Filtragem**: Organização dos dados e recomendações por perfil de investimento.
3. **Looping e Agendamento**: Processamento sequencial com nó `Loop Over Items` e intervalo (`Wait`) de 15 segundos para conformidade com o Rate Limit do Gemini.
4. **Geração via IA**: Criação do assunto e corpo do e-mail ajustados ao perfil.
5. **Tratamento do Output**: Higienização da resposta e formatação JSON/HTML.
6. **Envio do E-mail**: Disparo individualizado via Gmail.

## 📁 Como Importar o Workflow
1. Faça o download do ficheiro `workflow-rpa-investimentos.json` presente neste repositório.
2. No seu painel do n8n, clique em **Workflows** > **Import from File**.
3. Configure as credenciais da API do Google Gemini e do Gmail.
