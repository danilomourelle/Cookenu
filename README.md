> Status do Projeto: Concluido :heavy_check_mark:
## Danilo Mourelle
<p align="justify">Atualmente um desenvolverdor Web Fullstack (NodeJS), tenho 3 anos de experiência em programação de robôs industriais, onde desenvolvi habilidade na área de programação de linguagens de alto nível e lógica de programação. Também fiz parte, por 4 anos, de um grupo de pesquisa científica em sistemas neurais com foco em memória, aprendizado e Doença de Alzheimer onde obtive familiaridade com documentações em lingua inglesa e a repetibilidade de protocolos pré-estabelecidos.</p>

**Canais de comunicação**:
- [Linkedin](https://www.linkedin.com/in/danilomourelle/)
- [Github](https://github.com/danilomourelle)
- <danilomourelle@outlook.com>

## Labenu | Full-Stack Web Development Bootcamp
Desenvolvimento de aplicações completas, incluindo frontend Web com React e backend com Node.js.

[![Screenshot_1](https://raw.githubusercontent.com/danilomourelle/Whats4/master/Lbn.png)](https://www.labenu.com.br/)

# Cookenu

<br>
<p align="center">
  <img alt="GitHub top language" src="https://img.shields.io/github/languages/top/danilomourelle/Cookenu">

  <img alt="GitHub language count" src="https://img.shields.io/github/languages/count/danilomourelle/Cookenu">

  <img alt="Repository size" src="https://img.shields.io/github/repo-size/danilomourelle/Cookenu">

  <a href="https://github.com/danilomourelle/Cookenu/commits/master">
    <img alt="GitHub last commit" src="https://img.shields.io/github/last-commit/danilomourelle/Cookenu">
  </a>
</p>
<br>

#### Escopo do Projeto

<p align="justify">De manhã, você acordou, tomou uma bela xícara de café, verificou sua caixa de email e viu que tinha mais uma proposta de <em>Freela</em>. <em>Freela</em> vem de <em>Freelancer</em>, que é um trabalhador autônomo que sempre trabalha em projetos diferentes. Dessa vez, um cliente deseja te pagar muito bem para implementar o <strong>Cookenu</strong>.

</p>

<p align="justify">Esse produto nada mais é do que uma rede social, na qual os usuários podem dividir informações relevantes sobre comidas e receitas que tenham experimentado. Ela possui todas as funcionalidades mais comuns em redes sociais:</p>


1. **Cadastro:**
    - Como o projeto está no início, o usuário só precisa informar: o id, e-mail, nome a sua senha para realizar o cadastro. A senha tem uma regra: ela deve conter, no mínimo, 6 carácteres.

2. **Login:**
    - Como o projeto está no início, o usuário só precisa informar: o id, e-mail, nome a sua senha para realizar o cadastro. A senha tem uma regra: ela deve conter, no mínimo, 6 carácteres.
    
3. **Informações do próprio perfil:**
    - A partir do token de autenticação fornecido no login, o usuário deve ser capaz de ver as suas informações não sensíveis salvas no banco (vulgo, id e email)
    
4. **Criar receitas:**
    - O usuário deve poder criar uma receita. A receita deve ter os seguintes atributos: título, descrição/modo de preparo e data de criação
   
5. **Seguir usuário:**
    - Um usuário deve poder seguir outros usuários. Para isso, ele deve fornecer o id do usuário que deseja seguir. Atente-se que essa funcionalidade se assemelha ao do instagram: um usuário seguir outro, não significa que "esse outro" está seguindo o primeiro.
    
6. **Feed:**
    - Um usuário deve poder visualizar as receitas criadas pelos usuários que ele segue. As receitas devem estar ordenadas pela data de criação.

### LINGUAGENS

* Typescript
* SQL

### TECNOLOGIAS/FERRAMENTAS

* Git
* Typescript
* Node.js
* MVC
* Programação Orientada a Objeto
* MySQL
* Postman

### O que a plataforma é capaz de fazer :checkered_flag:

:trophy: Fornecer uma aplicação backend para um sistema de rede social voltada para o ambiente culinário 

:trophy: Coletar, verificar, armazenar os dados em banco de dados próprio para o sistema

:trophy: Criar, ler, atualizar e deletar (CRUD) dados da aplicação.

### Linguagens e libs utilizadas :books:

- [Typescript](https://www.typescriptlang.org/docs/home.html): versão 3.8.3
- [bcryptjs](https://styled-components.com/): versão 5.0.1 @types/2.4.2
- [dotenv](https://github.com/motdotla/dotenv): versão 8.2.0
- [express](https://expressjs.com/): versão 4.17.0 @types/4.17.0
- [jsonwebtoken](https://github.com/auth0/node-jsonwebtoken): versão 8.5.1 @types/8.3.9 
- [knex](http://knexjs.org/): versão 0.21.1 @types/0.16.1
- [moment](https://momentjs.com/): versão 2.25.3 
- [mysql](https://github.com/mysqljs/mysql): versão 2.18.1
- [uuid](https://github.com/uuidjs/uuid): versão 8.0.0 @types/7.0.3

### Como rodar a aplicação :arrow_forward:

No terminal, clone o projeto: 

```
git clone https://github.com/danilomourelle/Cookenu.git
```
Navegue para dentro da raiz do projeto
```
cd Cookenu
```
Instale as dependências
```
npm i
```
Crie um arquivo __.env__ com as configurções do seu bando de dados (preferencialmente MySQL, caso deseje utilizar outro, adaptações no código e dependências serão necessárias)
```
DB_HOST = seu_endereço_host
DB_USER = seu_usuário
DB_PASSWORD = sua_sehna
DB_DATABASE_NAME = seu_banco_de_dados
JWT_KEY = chave_para_jwt
JWT_EXPIRE_TIME = tempo_expiração (exemplo: 15 minutes)
BCRYPT_COST = cost_encriptação (idealmente um valor minimo de 12)
```
Execute a aplicação
```
npm start
```
Você poderá utilizar os endpoints através de um cliente HTTP (ex. [Postman](https://www.postman.com/product/api-client/)) tendo o endereço [localhost:3003](http:localhost:3003) como URL base para as requisições. Para informações de cada endpoint disponível conferir a [documentação](https://documenter.getpostman.com/view/10578976/T17CEqm8?version=latest)

**Projeto inicialmente desenvolvido em 18/05/2020 [neste Repo](https://github.com/future4code/sagan-Cookenu-grupo1) em parceria com:**
* [Eloísa Fagundes](https://github.com/EloisaFagundes)

### ADICIONAL
#### Querys realizadas paras as criações de tabelas utilizando o MySQL Workbench

**Tabela Usuário**

```SQL
CREATE TABLE User (
  id varchar(255) PRIMARY KEY,
  email varchar(255) UNIQUE NOT NULL,
  password varchar(255) NOT NULL,
  role varchar(255) NOT NULL DEFAULT 'normal',
  name varchar(255) NOT NULL,
)
```

**Tabela de Receitas**
```SQL
CREATE TABLE Recipes (
  id varchar(255) PRIMARY KEY,
  title varchar(255) UNIQUE NOT NULL,
  description text NOT NULL,
  created_at bigint(20) NOT NULL,
  creator_user_id varchar(255) NOT NULL,
  FOREIGN KEY (creator_user_id) REFERENCES User (id)
)
```

**Tabela de Relação entre Usuários**
```SQL
CREATE TABLE UserFollowConnection (
  followed_id varchar(255) NOT NULL,
  follower_id varchar(255) NOT NULL,
  FOREIGN KEY (followed_id) REFERENCES User (id),
  FOREIGN KEY (follower_id) REFERENCES User (id)
)
```


