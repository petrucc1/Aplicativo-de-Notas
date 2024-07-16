# Aplicativo de Notas

Este é um aplicativo de notas desenvolvido com Flask no backend e Angular no frontend. O projeto oferece endpoints em Flask para operações CRUD de notas, permitindo ao frontend realizar interações como criação, edição e exclusão de notas via requisições HTTP.

## Índice

1. [Funcionalidades](#funcionalidades)
2. [Pré-requisitos](#pré-requisitos)
3. [Instalação](#instalação)
4. [Configuração](#configuração)
5. [Como Usar](#como-usar)
6. [Estrutura do Projeto](#estrutura-do-projeto)
7. [Endpoints da API](#endpoints-da-api)
8. [Templates Angular](#templates-angular)

## Funcionalidades

- Criar novas notas
- Visualizar lista de notas
- Editar conteúdo das notas
- Excluir notas existentes

## Pré-requisitos

Antes de começar, certifique-se de ter os seguintes requisitos:

- Python 3.x
- Node.js e npm
- Angular CLI

## Instalação

Clone o repositório:
```bash
git clone https://github.com/seu-usuario/aplicativo-notas.git
cd aplicativo-notas
```

## Configuração

1. Backend (Flask)
    Navegue até o diretório `backend`:
    ```bash
    cd backend
    ```

    Instale as dependências:
    ```bash
    pip install -r requirements.txt
    ```

    Configure a URI do banco de dados no arquivo `.env`:
    ```bash
    MONGO_URI=sua_uri_do_mongodb
    ```

2. Frontend (Angular)
    Navegue até o diretório `frontend`:
    ```bash
    cd frontend
    ```

    Instale as dependências:
    ```bash
    npm install
    ```

## Como Usar

### Backend (Flask)

Inicie o servidor Flask:

    python app.py

O servidor estará rodando em `http://localhost:5000`.

### Frontend (Angular)

Inicie o servidor Angular:

    ng serve

O frontend estará disponível em `http://localhost:4200`.

## Estrutura do Projeto

A estrutura do projeto é organizada da seguinte forma:

```
aplicativo-notas/
├── backend/
│   ├── app.py
│   ├── models/
│   │   └── note.py
│   ├── routes/
│   │   └── api.py
│   └── requirements.txt
└── frontend/
    ├── src/
    │   ├── app/
    │   │   ├── components/
    │   │   │   ├── note-list/
    │   │   │   │   ├── note-list.component.html
    │   │   │   │   ├── note-list.component.ts
    │   │   │   │   └── note.service.ts
    │   │   │   ├── note-create/
    │   │   │   │   ├── note-create.component.html
    │   │   │   │   ├── note-create.component.ts
    │   │   │   │   └── note.service.ts
    │   │   │   └── ...
    │   │   ├── models/
    │   │   │   └── note.model.ts
    │   │   ├── services/
    │   │   │   └── note.service.ts
    │   │   ├── app-routing.module.ts
    │   │   ├── app.component.html
    │   │   ├── app.component.ts
    │   │   └── app.module.ts
    │   ├── index.html
    │   └── ...
    ├── angular.json
    ├── package.json
    └── ...
```

## Endpoints da API
* `GET /api/notes`: Retorna todas as notas cadastradas.
* `POST /api/notes`: Cria uma nova nota.
* `GET /api/notes/`: Retorna uma nota específica pelo ID.
* `PUT /api/notes/`: Atualiza uma nota existente pelo ID.
* `DELETE /api/notes/`: Exclui uma nota pelo ID.

## Templates Angular
* `note-list.component.html`: Template para listar todas as notas.
* `note-create.component.html`: Formulário para criar uma nova nota.
