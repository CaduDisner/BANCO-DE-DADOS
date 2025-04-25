# 🧩 Componentes principais de um Banco de Dados

## 1. 🧠 **SGBD (Sistema de Gerenciamento de Banco de Dados)**

> **É o software que gerencia tudo.**

O SGBD (ou em inglês, **DBMS - Database Management System**) é o **cérebro do banco de dados**. Ele controla:

* O armazenamento dos dados;
* Quem pode acessar o quê;
* Como os dados são organizados;
* Como garantir que os dados estão corretos.

🧱 Exemplos de SGBDs:

* MySQL
* PostgreSQL
* SQLite
* Oracle
* Microsoft SQL Server
* MongoDB (para bancos NoSQL)

***

## 2. 📦 **Banco de Dados em si (o repositório de dados)**

> **É o “ambiente” dentro do SGBD onde os dados vivem.**

É dentro do SGBD que você **cria um banco de dados**, que nada mais é que um **conjunto de tabelas, índices, relacionamentos, procedimentos, etc.**

🔹 Um único SGBD pode conter vários bancos de dados.\
Exemplo: um servidor MySQL pode ter:

* `loja_virtual`
* `sistema_escolar`
* `app_financeiro`

***

## 3. 📊 **Tabelas**

> **Onde os dados realmente são armazenados (em colunas e linhas).**

A tabela é a estrutura principal de armazenamento de dados **nos bancos relacionais**. Ela funciona como uma planilha com:

* **Colunas (campos)**: definem o tipo de informação (ex: nome, idade, email).
* **Linhas (registros)**: os dados propriamente ditos.

🔹 Exemplo de tabela `clientes`:

| id | nome        | email           |
| -- | ----------- | --------------- |
| 1  | João Silva  | joao@email.com  |
| 2  | Maria Souza | maria@email.com |

***

## 4. 🔑 **Chaves (Primária e Estrangeira)**

> **Mantêm a integridade e conexão entre dados.**

* **Chave Primária (Primary Key)**: identifica **unicamente** cada linha.\
  Exemplo: o `id` do cliente.
* **Chave Estrangeira (Foreign Key)**: conecta uma tabela a outra.\
  Exemplo: a tabela `pedidos` pode ter `cliente_id` que aponta para `clientes.id`.

***

## 5. 📁 **Esquema (Schema)**

> **É o "projeto" do banco de dados.**

O **esquema** define:

* Quais tabelas existem;
* Quais são os nomes dos campos;
* Como elas se relacionam;
* Tipos de dados de cada campo;
* Restrições (ex: não permitir valores nulos)

***

## 6. 🔤 **Tipos de Dados**

> **Definem que tipo de informação cada campo pode guardar.**

Exemplos comuns:

* `INT`: número inteiro
* `VARCHAR(n)`: texto com até n caracteres
* `DECIMAL`: números com casas decimais (ex: preços)
* `DATE`: data
* `BOOLEAN`: verdadeiro ou falso

Isso evita erros, como tentar armazenar letras onde deveria ser um número.

***

## 7. 🧾 **Índices**

> **Aceleram as buscas nos dados.**

Índices funcionam como atalhos para o banco **encontrar rapidamente os dados**.

🔹 Exemplo:

* Você cria um índice no campo `email`, e ao buscar por um email específico, a resposta vem muito mais rápido.

***

## 8. 🛠️ **Comandos SQL**

> **Linguagem usada para interagir com o banco.**

A linguagem padrão para bancos relacionais é a **SQL (Structured Query Language)**.

Principais comandos:

* `CREATE`: cria tabelas ou bancos
* `INSERT`: adiciona dados
* `SELECT`: busca dados
* `UPDATE`: altera dados
* `DELETE`: remove dados

***

## 9. 🔐 **Controle de Acesso / Usuários**

> **Define quem pode acessar o quê.**

Você pode:

* Criar usuários diferentes;
* Dar permissões (somente leitura, escrita, ou administração);
* Restringir tabelas ou operações.

🔒 Isso é essencial para **segurança**, especialmente em sistemas com muitos usuários.

***

## 10. 🗃️ **Backup e Recuperação**

> **Componente crítico para proteção contra falhas.**

Os bancos modernos permitem:

* **Backups automáticos** (diários, semanais...);
* **Recuperação de dados perdidos** por falhas, erros ou exclusões acidentais.

***

## 11. 🔄 **Transações**

> **Agrupam operações que devem ser executadas juntas.**

Imagine uma compra online:

* Debita o estoque
* Registra o pedido
* Atualiza o status do pagamento

Se uma parte falhar, o banco pode **reverter tudo**, garantindo integridade.

***

## 12. 🧩 (No caso de NoSQL) - Coleções, Documentos, Chave-Valor...

> Para bancos **não relacionais**, os componentes mudam um pouco.

Exemplo com MongoDB (banco NoSQL):

* **Coleções**: parecidas com tabelas
* **Documentos**: registros em formato JSON
* **Campos aninhados**: permitem estruturas complexas

***

## ✅ **Resumo dos Componentes**

| COMPONENTES        | FUNÇÃO PRINCIPAL                                |
| ------------------ | ----------------------------------------------- |
| SGBD               | Software que gerencia tudo                      |
| Banco de Dados     | Conjunto de tabelas e estruturas                |
| Tabelas            | Onde os dados são armazenados                   |
| Chaves             | Garantem integridade e relacionamentos          |
| Esquema            | Projeto estrutural do banco                     |
| Tipos de Dados     | Controlam o tipo e formato dos dados            |
| Índices            | Aceleram buscas                                 |
| SQL                | Linguagem de consulta e manipulação             |
| Usuários/Acessos   | Controle de permissões e segurança              |
| Backup/Recuperação | Proteção contra perdas de dados                 |
| Transações         | Confiabilidade em operações múltiplas           |
| (NoSQL) Coleções   | Alternativa a tabelas em bancos não relacionais |
