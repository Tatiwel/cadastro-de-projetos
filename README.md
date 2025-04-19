# Projeto Cadastro de Projetos

Este repositório principal contém dois submódulos: **backend** e **frontend**.

## Visão Geral

- **Repositório principal**: contém a configuração geral e os submódulos do projeto.
- **Submódulos**:
  - `cadastrodeprojetos.backend`: código do backend em FastAPI e PostgreSQL.
  - `cadastrodeprojetos.frontend`: código do frontend em PHP e Bootstrap.

## Pré-requisitos

Antes de clonar o projeto, certifique-se de ter instalado em sua máquina:

- Git (versão 2.20 ou superior)
- Docker e Docker Compose (opcional, para ambiente de desenvolvimento)

## Clonando o Repositório com Submódulos

Para clonar o repositório principal juntamente com os submódulos, execute:

```bash
git clone --recurse-submodules https://github.com/Tatiwel/cadastro-de-projetos.git
```

Isso criará a pasta `cadastro-de-projetos/` e inicializará automaticamente os submódulos:

- `cadastro-de-projetos/cadastrodeprojetos.backend/`
- `cadastro-de-projetos/cadastrodeprojetos.frontend/`

### Caso Já Tenha Clonado Sem Submódulos

Se você já clonou o repositório sem usar `--recurse-submodules`, basta inicializar e atualizar manualmente os submódulos:

```bash
git submodule update --init --recursive
```

## Estrutura de Diretórios

```
cadastro-de-projetos/
├── cadastrodeprojetos.backend/   # Submódulo: Backend (FastAPI + PostgreSQL)
└── cadastrodeprojetos.frontend/  # Submódulo: Frontend (PHP + Bootstrap)
```

## Trabalhando com os Submódulos

Para entrar no diretório do backend:

```bash
cd cadastrodeprojetos.backend
```

Para entrar no diretório do frontend:

```bash
cd cadastrodeprojetos.frontend
```

Cada submódulo possui seu próprio `README` com instruções de instalação e configuração específicas.

## Atualizando Submódulos

Para buscar as últimas alterações de todos os submódulos:

```bash
git pull --recurse-submodules
git submodule update --remote --merge
```

## Contribuindo

1. Faça um fork deste repositório.
2. Crie uma branch de recurso (`git checkout -b feature/nome-do-feature`).
3. Faça suas alterações e commit (`git commit -m "Descrição da mudança"`).
4. Envie para o seu fork (`git push origin feature/nome-do-feature`).
5. Abra um Pull Request.

## Licença

Este projeto está licenciado sob a [MIT License](LICENSE).