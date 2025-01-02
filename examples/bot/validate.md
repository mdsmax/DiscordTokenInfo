# Validação de Token (validate)

## Endpoint

**POST** `/api/bot/validate`

---

## Descrição
Verifica se o token fornecido é válido e retorna informações básicas sobre o bot associado, caso seja válido. Também trata erros como token inválido ou rate limitado.

---

## Parâmetros da Requisição

**Body**
```json
{
  "token": "seu_token_aqui"
}
```

---

## Respostas

### Sucesso (200)
```json
{
  "valid": true,
  "message": "Token válido!",
  "bot": {
    "id": "123456789012345678",
    "username": "MeuBot",
    "discriminator": "1234",
    "avatar": "https://cdn.discordapp.com/avatars/123456789012345678/abc123.png"
  }
}
```

### Token Inválido (401)
```json
{
  "valid": false,
  "error": "Token inválido."
}
```

### Rate Limited (429)
```json
{
  "valid": false,
  "error": "Rate limit excedido. Tente novamente mais tarde."
}
```

### Erro Desconhecido (500)
```json
{
  "valid": false,
  "error": "Erro interno no servidor."
}
```

---

## Observações

- O token fornecido deve ser um token válido de bot.
- Trate a resposta do endpoint para informar ao usuário sobre o estado do token.
- Caso esteja rate limitado, inclua um sistema de retry em seu cliente para evitar falhas subsequentes.
