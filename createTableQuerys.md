## Querys realizadas paras as criações de tabelas utilizando o MySQL Workbench

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