### Iniciar um projeto

`npm init -y`

### Instalar o Express

`npm install express`

### Instalar o Nodemon
Para desenvolvimento ele atualiza automaticamente o servidor em tempo de execução, sem necessidade de reiniciá-lo

`npm install nodemon -D`
Desta forma ele será instalado como devDependencies.

Inclua

```json
"scripts":{
    "start": "nodemon server.js",
}
```

Execute 
`npm start`

### Estrutura básica de pastas

```bash
meu-app/
├── 📄 .env                 # Variáveis de ambiente (sensíveis: DB_URL, PORT)
├── 📄 .gitignore           # Arquivos a ignorar (node_modules, .env) [1]
├── 📄 package.json         # Dependências e scripts do projeto [4]
├── 📄 package-lock.json    # Versões travadas das dependências [5]
├── 📄 server.js            # Ponto de entrada (inicia o servidor) [6]
└── 📂 src/                 # Código fonte da aplicação
    ├── 📂 controllers/     # Lógica de manipulação de requisições
    ├── 📂 database/        # Configuração de conexão com banco
    ├── 📂 middlewares/     # Middlewares (autenticação, logs, validação)
    ├── 📂 models/          # Definição dos esquemas de dados
    └── 📂 views/           # Arquivos de visualização (se necessário)
```

### Como usar o arquivo .env

Suponha que temos a variavel 

`PORT=3000`

E vamos utiliza-la no server.js

No server devemos importar

``require('dotenv').config``

E usar a variavel

`const PORT = process.env.PORT `

### Dependências

As dependências necessárias para o desenvolvimento do sistema já estão configuradas no package.json

São elas:

```JSON
"dependencies": {
    "bcryptjs": "^3.0.3",
    "connect-flash": "^0.1.1",
    "connect-sqlite3": "^0.9.16",
    "csrf-sync": "^4.2.1",
    "dotenv": "^17.3.1",
    "ejs": "^4.0.1",
    "express": "^5.2.1",
    "express-session": "^1.19.0",
    "helmet": "^8.1.0",
    "sqlite3": "^5.1.7",
    "validator": "^13.15.26"
  },
  "devDependencies": {
    "nodemon": "^3.1.14"
  }
```