# DESAFIO 

![Class](./assets/class_diagram.png)

## Problemas existentes 

- **Performance**
  - Falta de índices
  - findAll e obtem primeiro motorista em memória

- **Qualidade**
  - Falta testes
  - Design com muitas camadas desnecessárias
  - Aplicação de design patterns distorcidos
  - Bugs
    - Phantom write ao solicitar motorista

- **Segurança**
  - Não validar autenticidade do motorista
  - alterar status da corrida de outro motorista
  - vazamento de dados (motoristas e passageiros)

## O que vamos aprender?

- Arquitetura de soluções (com EC)
- Didática de código
  - Design de código
  - Gestão de código legado
- Design de API
- Segurança
- Estratégia de testes
