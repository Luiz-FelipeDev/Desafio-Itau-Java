# Solução - desafio backend java

## Descrição do Projeto


O projeto em questão é a sua solução de um desafio proposto pelo Itaú para uma Vaga de Desenvolvimento Backend Java. Abaixo deixo o link do desafio para que você posso lê-lo e realizá-lo também


[Desafio Backend Java Itaú](https://github.com/feltex/desafio-itau-backend/tree/main)

## Endpoints da API

A seguir serão especificados os endpoints que devem estar presentes na sua API e a funcionalidade esperada de cada um deles.

### Receber Transações : `POST /transacao`

Este é o endpoint que irá receber as Transações. Cada transação consiste de um valor e uma dataHora de quando ela aconteceu:

```json
{
    "valor": 123.45,
    "dataHora": "2020-08-07T12:34:56.789-03:00"
}
```

#### Validações realizadas

- [X] Valida transações para que não acontecam no futuro
- [X] Retorno de excessões para caso haja uma validação negativa no corpo da requisição
- [X] Transação valida valores maiores ou iguais a zero


1. Respostas dos Endpoints
   *  `201 Created` - A transação foi aceita
   * `422 Unprocessable Entity` - A transação não foi aceita por qualquer motivo de validação
   *  `400 Bad Request` - A APi não compreendeu a requisição do cliente


### Calcular Estatísticas : `GET /estatistica`

Este endpoint deve retornar estatísticas das transações que aconteceram nos últimos 60 segundos (1 minuto). As estatísticas que devem ser calculadas são:

```json
{
    "count": 10,
    "sum": 1234.56,
    "avg": 123.456,
    "min": 12.34,
    "max": 123.56
}
```


### Limpar Transações : `DELETE /transacao`

Este endpoint simplesmente apaga todos os dados de transações que estejam armazenados.

2. Resposta do Endpoint
   *  `200 OK` - Todas as informações acerca de estatística das transações foram apagas com sucesso


### Extras Implementados

- [X] **Logs**: A aplicação a cada operação realizada retorna logs para informar o que está acontecendo enquanto ela trabalha
- [X] **Tratamento de Erros**: Realização de tratamento de excessões para a retorno coerente dos dados de métricas das estatísticas

### O que desejo implementar no futuro

- [ ] **Documentação da API**: Utilizar futuramente Swagger para documentação da API
- [ ] **Containerização**: disponibilizar minha aplicação como um container
- [ ] **Implementação de Testes**: Utilizar testes utilitários e automatizados 

    


