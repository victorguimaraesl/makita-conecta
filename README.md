# Makita Conecta

Bem-vindo ao Makita Conecta! Este é um guia completo para configurar e rodar a aplicação localmente no seu computador.

O projeto é dividido em duas partes principais:

1. Backend (API): Uma API em Flask (Python) que gerencia o banco de dados (em memória, neste caso), o registro de usuários, a autenticação (login) e a segurança.

2. Frontend (Site): Uma aplicação em React (Vite + TypeScript) que o usuário vê e com a qual interage no navegador.

Para que a aplicação funcione, ambas as partes devem estar rodando ao mesmo tempo em terminais separados.

Pré-requisitos

Antes de começar, garanta que você tenha os seguintes programas instalados:

- Python (Versão 3.8 ou superior)

- Node.js (Versão 18 ou superior, que inclui o npm)

# Como Rodar a Aplicação (Passo a Passo)

Siga estes passos em ordem. Vamos começar ligando o "cérebro" (o backend) e depois a "face" (o frontend).

## Parte 1: Iniciar o Backend (API Flask)

O backend é responsável por lidar com os dados e a lógica de login/cadastro.

### 1. Abra seu Terminal:
Abra um novo terminal (Prompt de Comando, PowerShell, Terminal, etc.).

### 2. Navegue até a pasta do Backend:
Use o comando cd para entrar na pasta do backend.

```
# Exemplo:
cd C:\Caminho\Para\O\Projeto\makita-conecta-backend-main
```

### 3. Crie um Ambiente Virtual:
Isso cria uma pasta venv que isola as dependências do Python.

```
python -m venv venv
```

### 4. Ative o Ambiente Virtual:
Você precisa "ligar" o ambiente antes de instalar coisas nele.

- No Windows (PowerShell/CMD):

```
.\venv\Scripts\activate
```

- No macOS / Linux:

```
source venv/bin/activate
```

- (Você saberá que funcionou se vir (venv) no início da linha do seu terminal).

### 5. Instale as Dependências do Python:
Com o venv ativo, instale o Flask e os outros pacotes necessários.

```
pip install flask flask-cors flask-bcrypt Flask-JWT-Extended
```

### 6. Inicie o Servidor da API:
Este é o comando final para ligar o backend.

```
python -m flask run
```

(Se tudo der certo, o terminal vai "travar" e mostrar que está rodando em http://127.0.0.1:5000).

DEIXE ESTE TERMINAL ABERTO! Se você fechá-lo, a API desliga.

## Parte 2: Iniciar o Frontend (React)

Agora, em uma nova janela de terminal, vamos ligar o site que o usuário vê.

### 1. Abra um SEGUNDO Terminal:
Não feche o primeiro! Abra um novo.

### 2. Navegue até a pasta do Frontend:
Use o comando cd para entrar na pasta do frontend.

```
# Exemplo:
cd C:\Caminho\Para\O\Projeto\makita-conecta-frontend-main
```

### 3. Instale as Dependências do Node:
Este comando lê o arquivo package.json e baixa todos os pacotes do React.

```
npm install
```

### 4. Inicie o Servidor do Frontend:
Este comando liga o site em modo de desenvolvimento.

```
npm run dev
```

(O terminal mostrará que o site está rodando, geralmente em http://localhost:5173).

DEIXE ESTE SEGUNDO TERMINAL ABERTO TAMBÉM!

# Pronto!

Se os dois terminais estiverem rodando (o Backend na porta 5000 e o Frontend na porta 5173), a aplicação está funcionando!

Agora, você pode:

1. Abrir seu navegador (Chrome, Firefox, etc.).

2. Acessar o endereço do Frontend: http://localhost:5173.

3. Tentar criar uma nova conta e fazer login.

O site (Frontend) irá automaticamente enviar as requisições para a API (Backend) que está rodando na porta 5000.
