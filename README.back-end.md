# 📁 Cadastro de Projetos – Back-end com Pyton e FastAPI

Este projeto é um sistema de gerenciamento de projetos desenvolvido com **FastAPI**, utilizando **PostgreSQL** como banco de dados e **SQLAlchemy** como ORM. O sistema oferece as operações básicas de CRUD para facilitar a administração de projetos.

---

## 🔧 Funcionalidades

- **Listagem de Projetos:** Exibe todos os projetos cadastrados.
- **Criação de Novo Projeto:** Permite o cadastro de novos projetos.
- **Edição de Projeto Existente:** Possibilita a atualização das informações de projetos já cadastrados.
- **Remoção de Projeto:** Permite excluir projetos indesejados.
- **Visualização de Detalhes:** Mostra informações detalhadas sobre um projeto específico.

---

## 👨‍💻 Tecnologias Utilizadas

- **Backend:** FastAPI
- **Banco de Dados:** PostgreSQL
- **ORM:** SQLAlchemy

---

## 🏠 Estrutura do Projeto

- **Módulo Raiz:** [cadastro-de-projetos](https://github.com/Tatiwel/cadastro-de-projetos.git)
- **Submódulo Backend:** [cadastrodeprojetos.backend](https://github.com/Tatiwel/cadastrodeprojetos.backend.git)

---

## ⚙️ Configuração do Ambiente

O projeto usa dois arquivos de variáveis de ambiente:

### `.env.development` (para uso local com `uvicorn`)

```env
DATABASE_URL=postgresql://[USUARIO]:[SENHA]@localhost:[PORTA]/[NOME_DO_BANCO]
```

### `.env.docker` (para uso com `Docker Compose`)

```env
DATABASE_URL=postgresql://[USUARIO]:[SENHA]@db:[PORTA]/[NOME_DO_BANCO]
```

Altere as credenciais conforme necessário (usuario, senha, nome_do_banco, porta, etc.)

## 🚀 Execução do Projeto

- ### 🖥️ Rodar Localmente (LocalHost)

  1. Ative o ambiente virtual e instale as dependências:
     ```python
      pip install -r requirements.txt
     ```
  2. Execute a aplicação com reload:
     ```python
      uvicorn app.main:app --reload
     ```
  3. Ou se preferir utilizar os comandos simplificados encontrados no `run.py` na raiz no projeto:

     - ▶️ Iniciar a API localmente:
       ```python
        python run.py run
       ```
     - 📑 Abre a documentação no navegador
       ```python
        python run.py docs
       ```
     - 🧪 Testes

       ```python
        python run.py test
       ```

- ### 🐳 Usando Docker

  1. Antes de criar uma imagem, é necessário configurar uma variável de ambiente (`.env`) e mapear a conexão com **local host interno** do docker, definido pelo comando `host.docker.internal`:

  ```env
    DATABASE_URL=postgresql://[USUARIO]:[SENHA]@host.docker.internal:[PORTA]/[NOME_DO_BANCO]
  ```

  2. Crie imagem a partir do Dockerfile:

  ```bash
    docker build -t my-username/my-image .
  ```

  3. Rodar a imagem manualmente (**Aponte o `.env` criado como parâmetro após o termo `--env-file`**)

  ```bash
    docker run -p 8000:8000 --env-file .env.docker my-username/my-image
  ```

  4. Verificar imagens criadas:

  ```bash
    docker images
  ```

  5. Verificar TODOS os contêineres (ativos e parados)

  ```bash
    docker ps -a
  ```

- ### 🧩 Usando Docker Compose

  1. Subir os serviços (API e banco de dados PostgreSQL):

  ```bash
    docker-compose up --build
  ```

  2. Parar os serviços:

  ```bash
    docker-compose down
  ```

  3. Reiniciar os serviços (sem rebuild):

  ```bash
    docker-compose restart
  ```

  4. Recriar do zero:

  ```bash
    docker-compose down -v
    docker-compose up --build
  ```

  5. Verificar imagens criadas:

  ```bash
    docker images
  ```

  6. Verificar TODOS os contêineres (ativos e parados)

  ```bash
    docker ps -a
  ```

## 📄 Documentação Swagger

- Após subir o projeto com qualquer método (Docker ou local), acesse:

```bash
  http://localhost:8000/docs
```
