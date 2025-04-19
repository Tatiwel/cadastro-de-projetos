# 📁 Cadastro de Projetos – Front-end PHP e Bootstrap

Este é o front-end de uma aplicação CRUD de projetos desenvolvida em PHP puro, que consome uma API REST construída com FastAPI. A interface utiliza o Bootstrap 5 para estilização e oferece funcionalidades completas para gerenciamento de projetos.

---

## 🔧 Funcionalidades

- Listar todos os projetos cadastrados.
- Criar novos projetos através de um formulário.
- Editar projetos existentes.
- Visualizar detalhes completos de um projeto.
- Deletar projetos com confirmação.

---

## 👨‍💻 Tecnologias Utilizadas

- PHP 7.4+ (para o back-end da interface).
- Bootstrap 5 (para estilização responsiva).
- JavaScript (para interatividade no front-end).
- FastAPI (API REST consumida pela aplicação).

---

## 🏠 Estrutura do Projeto

- **Módulo Raiz:** [cadastro-de-projetos](https://github.com/Tatiwel/cadastro-de-projetos.git)
- **Submódulo Backend:** [cadastrodeprojetos.backend](https://github.com/Tatiwel/cadastrodeprojetos.backend.git)

---

## ⚙️ Pré-requisitos

- Servidor web configurado (ex.: Apache ou Nginx).
- PHP 7.4 ou superior instalado.
- Python 3.8+ com FastAPI e Uvicorn para a API.
- Conexão com a API FastAPI rodando em `http://127.0.0.1:8000`.

---

## 🚀 Como Executar

1. Clone o repositório:

   ```bash
   git clone https://github.com/Tatiwel/cadastrodeprojetos.frontend.git
   ```

2. Configure o servidor web:

   - Aponte o `DocumentRoot` para a pasta `cadastro-de-projetos`.
   - Certifique-se de que o servidor está interpretando arquivos `.php`.

3. Inicie a API FastAPI:

   ```bash
   uvicorn app.main:app --reload
   ```

   A API estará disponível em `http://127.0.0.1:8000`.

4. Acesse a aplicação:

   - Abra o navegador e vá para `http://localhost/pages/home.php`.

---

## 🧪 Testando a Aplicação

- **Listar projetos**: Acesse a página inicial para ver todos os projetos cadastrados.
- **Criar novo projeto**: Clique em "Criar Novo Projeto" e preencha o formulário.
- **Editar projeto**: Na listagem, clique em "Editar" ao lado do projeto desejado.
- **Visualizar detalhes**: Clique em "Detalhes" para ver informações completas do projeto.
- **Deletar projeto**: Clique em "Deletar" e confirme a exclusão.

---
