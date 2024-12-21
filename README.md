Vou criar um README específico para o exemplo4.py, que é um script de integração com a API da OpenAI. Aqui está o README adaptado:

````markdown:README.md
# OpenAI API Integration

Um script Python simples para interagir com a API da OpenAI, permitindo fazer requisições ao modelo GPT-3.5-turbo.

## 📋 Descrição

Este projeto demonstra como fazer requisições à API da OpenAI usando Python. O script permite enviar prompts para o modelo GPT-3.5-turbo e receber respostas em formato de texto.

## 🚀 Funcionalidades

- Integração com a API da OpenAI
- Envio de prompts para o modelo GPT-3.5-turbo
- Processamento de respostas da API
- Utilização de variáveis de ambiente para segurança

## 📦 Pré-requisitos

- Python 3.8+
- Uma chave de API da OpenAI

## 🛠️ Instalação

1. Clone o repositório:
```bash
git clone https://github.com/seu-usuario/openai-api-integration.git
cd openai-api-integration
```

2. Crie um ambiente virtual:
```bash
python -m venv venv
source venv/bin/activate  # Linux/Mac
# ou
venv\Scripts\activate  # Windows
```

3. Instale as dependências:
```bash
pip install -r requirements.txt
```

## ⚙️ Configuração

1. Crie um arquivo `.env` na raiz do projeto
2. Adicione sua chave da API da OpenAI:
```
OPENAI_API_KEY=sua_chave_api_aqui
```

## 📊 Uso

Execute o script com:
```bash
python exemplo4.py
```

## 📝 Requirements.txt

Crie um arquivo `requirements.txt` com as seguintes dependências:
```
requests==2.31.0
python-dotenv==1.0.0
```

## 🔍 Exemplo de Código

```python
import requests
import json
import os
from dotenv import load_dotenv

load_dotenv()

url = 'https://api.openai.com/v1/chat/completions'
openai_api_key = os.getenv('OPENAI_API_KEY')

headers = {
    'Content-Type': 'application/json',
    'Authorization': f'Bearer {openai_api_key}'
}

data = {
    'model': 'gpt-3.5-turbo',
    'messages': [{'role': 'user', 'content': 'Qual é a capital da França?'}]
}

response = requests.post(url, headers=headers, data=json.dumps(data))
print(response.json()['choices'][0]['message']['content'])
```

## ⚠️ Notas Importantes

- Mantenha sua chave API segura e nunca a compartilhe
- Certifique-se de ter créditos suficientes em sua conta OpenAI
- Verifique a documentação da OpenAI para limites de taxa e melhores práticas

## 👤 Autor

* **Seu Nome** - [seu-usuario-github](https://github.com/seu-usuario)

## 📄 Licença

Este projeto está sob a licença MIT - veja o arquivo [LICENSE.md](LICENSE.md) para detalhes.
````

Este README foi adaptado especificamente para o exemplo4.py, focando na integração com a API da OpenAI. Incluí:
- Uma descrição clara do propósito do script
- Instruções detalhadas de instalação
- Como configurar o arquivo .env
- O conteúdo necessário para o requirements.txt
- Um exemplo do código
- Notas importantes sobre segurança e uso da API

O arquivo requirements.txt especifica as duas principais dependências necessárias para executar o script:
- requests: para fazer as chamadas HTTP à API
- python-dotenv: para carregar as variáveis de ambiente do arquivo .env
