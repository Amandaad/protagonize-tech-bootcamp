# Desafio Técnico - Gerenciador de Tarefas

Aplicação full stack para cadastro e gerenciamento de tarefas com:

- Angular no front-end
- ASP.NET Core Web API no back-end
- SQL Server como banco de dados
- Entity Framework Core para persistência

## Estrutura do projeto

```text
PROTAGONIZE/
|-- backend/TaskManager.Api
|-- frontend
```

## Funcionalidades

- Listar tarefas
- Buscar tarefa por ID
- Criar tarefa
- Editar tarefa
- Excluir tarefa
- Filtrar tarefas por status
- Validação básica no formulário
- Mensagens simples de sucesso e erro

## Pré-requisitos

- .NET SDK 8.0 ou superior
- SQL Server
- Node.js 20+ ou 22+
- Angular CLI compatível com Angular 18

## Como rodar o back-end

1. Ajuste a string de conexão em `backend/TaskManager.Api/appsettings.json` se necessário.
2. No terminal, acesse:

```powershell
cd backend/TaskManager.Api
```

3. Restaure os pacotes:

```powershell
dotnet restore
```

4. Execute a API:

```powershell
dotnet run
```

Ao iniciar, a aplicação aplica as migrations automaticamente e cria o banco `TaskManagerDb` se a conexão estiver válida.

## Como rodar o front-end

1. No terminal, acesse:

```powershell
cd frontend
```

2. Instale as dependências:

```powershell
npm install
```

3. Inicie o projeto:

```powershell
npx ng serve
```

4. Acesse:

```text
http://localhost:4200
```

## Observações importantes

- O serviço Angular está apontando para `https://localhost:5001/api/tarefas` em `frontend/src/app/services/tarefa.service.ts`.
- Se a porta da API mudar, ajuste essa URL.
- O status aceito pela API é `Pendente` ou `Concluida`.
- O campo `DataCriacao` é definido automaticamente no back-end.

## Endpoints da API

- `GET /api/tarefas`
- `GET /api/tarefas/{id}`
- `POST /api/tarefas`
- `PUT /api/tarefas/{id}`
- `DELETE /api/tarefas/{id}`

## Exemplo de payload

```json
{
  "id": 0,
  "titulo": "Estudar ASP.NET Core",
  "descricao": "Implementar o CRUD de tarefas",
  "status": "Pendente"
}
```

## Limitação deste ambiente

Este workspace estava vazio e o ambiente atual não possui `dotnet` nem Angular CLI instalados globalmente, então a solução foi estruturada manualmente e não pôde ser executada/validada aqui. Com os pré-requisitos acima instalados, o projeto fica pronto para restauração, build e execução.
