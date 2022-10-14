# PR05 - Exclusão de professor

Abaixo você encontrará todas as informações necessárias para a implementação do caso de uso **Exclusão de professor**.

## Rotas

| Rota             | Método | Descrição                 |
| ---------------- | ------ | ------------------------- |
| /api/professores | DELETE | Exclui o professor logado |

## Rota DELETE /api/professores

### Requisição

**Query Parameters**

Não se aplica

**Headers**

| Campo         | Tipo   | Descrição       | Exemplo                                              |
| ------------- | ------ | --------------- | ---------------------------------------------------- |
| Authorization | string | Token de acesso | "Bearer 303Xs5g4co7glr4xtJHXHvbNI4Pl0y1hgyZZWOENHMx" |

**Body**

Não se aplica

### Resposta

**Status Code**

| Status Code | Descrição                      |
| ----------- | ------------------------------ |
| 204         | Exclusão realizada com sucesso |
| 401         | Token inválido                 |

**Body**

Não se aplica

### Exemplos

**Requisição**

```
DELETE /api/professores HTTP/1.1
Host: localhost:3000
Accept: application/json
Authorization: Bearer 303Xs5g4co7glr4xtJHXHvbNI4Pl0y1hgyZZWOENHMx
```

**Resposta com sucesso**

```
HTTP/1.1 204 No Content
```

**Resposta com token inválido**

```
HTTP/1.1 401 Unauthorized
Content-Type: application/json

{
  "message": "Token expirado",
  "status": 401,
  "error": "Unauthorized",
  "cause": "TokenExpiredError"
}
```
