---
id: InstallBackend
title: Preparando o ambiente de desenvolvimento (backend)
sidebar_label: Backend
---

## Requisitos:

---

- [Docker](https://docs.docker.com/install/linux/docker-ce/ubuntu/)
- [Docker Compose](https://docs.docker.com/compose/install/)
- [Poetry](https://poetry.eustace.io/docs/)

```sh
# Inicializar o banco de dados
sudo docker-compose up -d

# Configurações (editar se necessário)

cp .env.sample .env
#ou
cp .env_sample .env

# Instalar as dependências
poetry install
# Executar os comandos dentro do virtualenv (criado automaticamente)
poetry run python manage.py migrate
poetry run python manage.py runserver
```

O backend responde localmente na porta 8000: http://localhost:8000/api/v1/swagger/. Para mais detalhes sobre o seu funcionamento, leia o [README do diretório backend](backend/README.md).

## Commit

---

Para fazer um commit, você deve estar dentro do virtualenv do backend.

Use o poetry para isso:

```sh
poetry shell
```

Configure os hooks de commit para executar verificações de código antes de fazer um commit.

```sh
pre-commit install
```
