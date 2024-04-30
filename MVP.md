## REFERÊNCIAS

- [DESAFIO](CHALLENGE.md)
- [MVP](MVP.md)
- [RELEASE](RELEASE.md)
- [POSTMAN COLLECTION](https://l3l3co.postman.co/workspace/New-Team-Workspace~d450d5e4-7c3a-4449-9f65-226a04a3389e/collection/414153-735bc628-c41e-478c-a2c4-d90be0758a1a?action=share&creator=414153&active-environment=414153-4adc1ab7-8041-4b2c-8241-002c5e9dcfa7)
  

## REPOSITÓRIOS BASES

- [NODE]()
- [KOTLIN](https://github.com/jaya-academy/ridely-kotlin)


# MVP

Abaixo será apresentado o que é esperado e o que será entregue na primeira versão do projeto para todos o participantes do grupo de estudo e aprofundamento.

---

### Solicitar Motorista

[POST] /request-driver

> Request Body

```json
{
  "name": string,
  "email": string,
  "pickup": string,
  "dropoff": string
}
```


> Response Body

```json
{
  "id": string,
  "name": string,
  "license_plate": string,
  "model": string,
  "color" : string
}
```

---

### Cancelar corrida Passageiro


[DELETE] /cancelar-ride

> Request Body

```json
{
    "id": number
}
```

> Response Body

```json
{
  "id": number,
  "status": string
}
```

---

### Corrida Alocada

[GET] /get-rides

> Response Body

```json
{
    "id": number,
    "passageiro": {
        "email": string,
        "nome": string,
    },
    "endereco": string
}
```

---

### Recusar Corrida Motorista

[POST] /refuse-ride

> Request Body

```json
{
  "id": number
}
```

> Response Body

```json
{
  "id": number,
  "passageiro": {
    "email": string,
    "nome": string,
  },
  "endereco": string,
  "status": string
}
```

---

## Finaliar Corrida

[POST] /finish-ride

> Request Body

```json
{
  "id": number,
  "valor": number
}
```

> Response Body

```json
{
  "id": number,
  "passageiro": {
    "email": string,
    "nome": string,
  },
  "endereco": string,
  "status": string,
  "valor": number
}
```