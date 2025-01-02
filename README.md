# tokenmgr - a melhor API para gerenciar contas/aplicações do Discord

## Descrição Geral
Uma API desenvolvida para facilitar o gerenciamento de bots do Discord utilizando seu token. A API fornece endpoints para realizar operações como validação de tokens, manipulação de intents, alteração de informações do bot, e muito mais.

---

## Estrutura dos Endpoints

### **Base URL**
`https://tokenmgr.squareweb.app/api`

### **Endpoints Disponíveis**

| Método | Endpoint            | Descrição                               |
|--------|---------------------|-----------------------------------------|
| POST   | `/bot/validate`     | Valida um token de bot.                 |
| POST   | `/bot/info`         | Retorna informações do bot.             |
| POST   | `/bot/intents/list` | Lista as intents ativas.                |
| POST   | `/bot/intents/activate` | Ativa todas as intents.            |
| POST   | `/bot/change`       | Altera informações do bot.              |

---

## Exemplo de Uso

**Validação de Token**

**Requisição:**
```bash
curl -X POST https://tokenmgr.squareweb.app/api/bot/validate \
-H "Content-Type: application/json" \
-d '{ "token": "seu_token_aqui" }'
```

**Resposta:**
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

---

## Tecnologias Utilizadas

- **Express.js**
- **Axios**
- **TypeScript**

---
