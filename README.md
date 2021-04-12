![Logo do Markdown](imagesGit/img1.png)

## Sobre o projeto

Nesse projeto e possível adicionar um transação e visualizar todas as transações feitas, também e pode ser feita um transação para retirar o valor mas só e permitido se tiver o valor para retirar e também e permitido excluir um transação.
Api consome dados em json ou arquivo csv.

### Listagem de Transação

* Método GET

Ao fim da listagem de transação realizada com sucesso e possível visualizar um balanço onde tem os valores que entram em caixa, os que foram retirados e o total em caixa.

Body

* Response:
  * 200: Sucess

  body

  ```
    "transactions": [
    {
      "id": "3f37ed1b-5a21-48e9-bb66-f93723b02b7b",
      "title": "Loan",
      "type": "income",
      "value": "1500.00",
      "category_id": "7e0202b0-d032-4a85-96f7-0bcdce3e6b27",
      "created_at": "2020-12-17T03:11:33.597Z",
      "updated_at": "2020-12-17T03:11:33.597Z",
      "category": {
        "id": "7e0202b0-d032-4a85-96f7-0bcdce3e6b27",
        "title": "Others",
        "created_at": "2020-12-17T03:11:33.520Z",
        "updated_at": "2020-12-17T03:11:33.520Z"
      }
    }
  ],
  "balance": {
    "income": 3000,
    "outcome": 106,
    "total": 2894
  }
  ```

  * 400: Bad Request



### Criar Transação

* Método POST

Dados requeridos:

body

```
  {
    "title": "fff",
    "value": 1000.00,
    "type": "income",
    "category": "Conta"
  }
```

* response
  * 201: Created
  body

  ```
  {
  "title": "fff",
  "type": "income",
  "value": 1000,
  "category_id": "8094f3e3-a91b-4270-92fe-8271c32c7c77",
  "category": {
    "id": "8094f3e3-a91b-4270-92fe-8271c32c7c77",
    "title": "Conta",
    "created_at": "2020-12-16T04:42:44.928Z",
    "updated_at": "2020-12-16T04:42:44.928Z"
  },
  "id": "c0e8b9dd-f7db-4d22-9c7e-c66b7b5d2df3",
  "created_at": "2020-12-16T04:42:44.963Z",
  "updated_at": "2020-12-16T04:42:44.963Z"
  }

  ```

  * 400: Bad Request

### Deletar Transação

* Método DELETE

* Response:
  * 200: Sucess

  * 404: Not found


### Inicializar

1. Clonar repositorio: git clone
2. usar comando para baixar dependências: yarn
3. comando para iniciar servidor: yarn dev:server
