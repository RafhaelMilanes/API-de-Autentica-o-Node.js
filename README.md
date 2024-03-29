

## API de Autenticação Node.js com Express e MongoDB 🚀
Esta é uma API de autenticação básica construída com Node.js, Express, MongoDB e JWT (JSON Web Tokens).

## Funcionalidades

- Registro de usuário
- Login de usuário
- Autenticação de token JWT
- Rota privada para acessar informações do usuário

## Pré-requisitos

- Node.js instalado localmente
- Conta no MongoDB Atlas (ou outra instância MongoDB)
- Postman ou qualquer outra ferramenta para testar APIs

## Instalação

Clone o repositório

```javascript
git clone <https://github.com/RafhaelMilanes/API-de-Autentica-o-Node.js>

```

Instale as dependências:

```
cd autentificacaoNodeJs
npm install 
```

Configure as variáveis de ambiente:
Crie um arquivo .env na raiz do projeto e adicione as seguintes variáveis:

```
DB_USER=sua_usuario_do_MongoDB
DB_PASS=sua_senha_do_MongoDB
SECRET=sua_chave_secreta_para_o_JWT

```

Inicie o servidor:

```
npm start

```
A API estará disponível em http://localhost:3000.

## Endpoints

- POST /auth/register: Registra um novo usuário.
- POST /auth/login: Autentica um usuário e gera um token JWT.
- GET /user/:id: Retorna informações de um usuário específico. Rota protegida, requer um token JWT no cabeçalho Authorization.

## Exemplo de Requisição POST para Registro de Usuário

```
POST /auth/register
Content-Type: application/json

{
  "name": "Nome do Usuário",
  "email": "email@example.com",
  "password": "senha123",
  "confirmpassword": "senha123"
}

```

## Exemplo de Requisição POST para Login de Usuário

```
POST /auth/login
Content-Type: application/json

{
  "email": "email@example.com",
  "password": "senha123"
}


```
A resposta incluirá um token JWT que deve ser incluído nos cabeçalhos das solicitações protegidas.

## Usando o Postman

Você pode importar a coleção do Postman fornecida neste repositório para testar facilmente os endpoints da API. Basta abrir o Postman e seguir estas etapas:

Clique no botão "Importar" na barra de navegação do Postman.
Selecione a opção "Link" e cole o URL do arquivo da coleção do Postman: URL_DA_COLECAO.
Clique em "Continuar" e depois em "Importar".
Agora você terá uma coleção no Postman com todos os endpoints prontos para uso. Certifique-se de ajustar as variáveis de ambiente no Postman para corresponder às suas configurações locais.