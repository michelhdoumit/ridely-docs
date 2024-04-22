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