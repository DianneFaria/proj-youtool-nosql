<h1 align="center">
  Projeto NoSQL: Coleta de Dados do YouTube com youtool
</h1>

Projeto da disciplica Laboratório de Banco de Dados. O objetivo é coletar e armazenar dados do YouTube utilizando a API do YouTube e a biblioteca youtool.

## 🎯 Objetivos
* Utilizar a biblioteca youtool para acessar a API do YouTube e coletar dados.
* Armazenar os dados coletados em um banco de dados NoSQL (MongoDB).
* Aplicar conceitos aprendidos em NoSQL, manipulação de dados e integração com APIs externas.

## 📚 Canal de Análise
*  Escolhi o canal [GeekFreak](https://www.youtube.com/@aquelegf) para coletar os dados, o tema principal desse canal são livros.

## 🛠️ Tecnologias Usadas
* Python
* MongoDB (Banco de Dados NoSQL)
* youtool (biblioteca para interagir com a API do YouTube)

## 📁 Estrutura
- `project.py`                  : Script principal de coleta e processamento de dados
- `reset_db.py`                  : Reseta o banco caso necessário
- `requirements.txt`        : Arquivo com dependências do projeto
- `README.md`                Informações do projeto.
- `.gitignore`              : Arquivo para ignorar arquivos 

## 📖 Instruções 

### Pré-Requisitos
É necessário ter os seguintes requisitos:
- [Python](https://www.python.org/)
- [MongoDB](https://www.mongodb.com/)
- [API Keys](https://console.cloud.google.com/)

### Instruções para executar o projeto em sua máquina:

**0. Baixe os arquivos**

```bash
# Clone o repositório
$ git clone https://github.com/DianneFaria/proj-youtool-nosql
```
**1. Instale as dependências**

```
pip install -r requirements.txt
```
**2. Configure as variáveis de ambiente**

Crie um arquivo .env e adicione as variáveis de ambiente:

```
YOUTUBE_API_KEYS="chave_api1, chave_api2"
CHANNEL_URL="https://youtube.com/@seu-canal"
MONGO_URI="mongodb+srv://<user>:<senha>@cluster0.slcacxc.mongodb.net/..."
DB_NAME=name-database
SINCE=2024-01-01T00:00:00Z
TRANSCRIPTION_LANG=en
TRANSCRIPTION_DIR=./transcricoes
```

**3. Acesse 👉 [Google Cloud Console](https://console.cloud.google.com/)**

Crie suas chaves da API.

- Crie um novo projeto ("Novo Projeto").

- No menu lateral, vá em "API e Serviços" → "Biblioteca".

- Pesquise por "YouTube Data API v3" → clique → Ativar.

- Vá em "Credenciais" → "Criar credencial" → "Chave de API".

- Uma chave será gerada. Copie e guarde!

- Gere uma segunda chave para adicionar ao .env, assim você terá duas credências e não ficará sem créditos.


**4. Acesse 👉 https://www.mongodb.com/cloud/atlas e crie uma conta gratuita**

Crie seu banco no MongoDB.

- Clique em "Build a Database" → escolha Free (M0) → Create.

- Configure o cluster:

- Escolha região (pode ser a mais próxima, ex.: São Paulo).

- Crie um usuário do banco:

- Username: admin

- Password: sua_senha

- Configure acesso:

- Adicione seu IP (0.0.0.0 libera para qualquer IP ou configure seu IP local).

- Clique em "Connect" → "Connect your application".

- Copie sua string de conexão para usar no .env, ela será assim:

```
mongodb+srv://admin:sua_senha@cluster0.xxxxx.mongodb.net/
```

**5. Execute**
```
py project.py
```

<details>
  <summary>🎥 Resultados do projeto</summary>
	
  ### GIF de execução
  ![gif youtool](https://github.com/user-attachments/assets/b05732c4-2158-4559-a698-0a2493631a7a)

  ### Imagem do MongoDB
  ![image](https://github.com/user-attachments/assets/2e97aeb2-7154-4df2-8a2f-9afcbb39e1bc)


</details>





