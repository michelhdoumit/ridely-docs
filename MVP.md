## REFERÊNCIAS

- [DESAFIO](CHALLENGE.md)
- [MVP](MVP.md)
- [RELEASE](RELEASE.md)
- [POSTMAN COLLECTION](https://l3l3co.postman.co/workspace/New-Team-Workspace~d450d5e4-7c3a-4449-9f65-226a04a3389e/collection/414153-735bc628-c41e-478c-a2c4-d90be0758a1a?action=share&creator=414153&active-environment=414153-4adc1ab7-8041-4b2c-8241-002c5e9dcfa7)

## REPOSITÓRIOS BASES

- [NODE]()
- [KOTLIN](https://github.com/jaya-academy/ridely-kotlin)

# MVP

Abaixo será apresentado o que é esperado e o que será entregue na primeira versão do projeto para todos o participantes
do grupo de estudo e aprofundamento.

---

### Solicitar Motorista [Passageiro]

[POST] /rides/request-driver

> Request Body

```typescript
{
    passenger: {
        name: string;
        email: string;
    }
    pick_up: string;
    drop_off: string;
}
```

> Response Body

```typescript
{
    id: number;
    status: string;
    drop_off: string;
    pick_up: string;
    driver: {
        name: string;
        car: {
            color: string;
            license_plate: string;
            model: string
        }
    }
}
```

---

### Cancelar corrida [Passageiro]

[POST] /rides/cancel-ride

> Request Body

```typescript
{
  id: string
}
```

> Response Body

```typescript
{
    id: number;
    status: string;
    drop_off: string;
    pick_up: string;
}
```

---
### Buscar Corrida Alocada [Motorista]

[GET] /drivers/{id}/get-rides

> Response Body

```typescript
{
    id: number;
    status: string;
    drop_off: string;
    pick_up: string;
    passenger: {
        email: string;
        name: string;
    }
}
```

---

### Aceitar Corrida [Motorista]

[POST] /rides/accept-ride

> Request Body

```typescript
{
  id: string
}
```

> Response Body

```typescript
{
    id: number;
    status: string;
    drop_off: string;
    pick_up: string;
    passenger: {
        email: string;
        name: string;
    }
}
```

---

### Recusar Corrida [Motorista]

[POST] /rides/refuse-ride

> Request Body

```typescript
{
  id: number
}
```

> Response Body

```typescript
{
    id: number;
    status: string;
    drop_off: string;
    pick_up: string;
    passenger: {
        email: string;
        name: string;
    }
}
```

---

## Finalziar Corrida [Motorista]

[POST] /rides/finish-ride

> Request Body

```typescript
{
    id: number;
    price: number;
}
```

> Response Body

```typescript
{
    id: number;
    status: string;
    drop_off: string;
    price: number;
    passenger: {
        email: string;
        name: string;
    }
}
```