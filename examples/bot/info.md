## Endpoint: /bot/info

### **Descrição:**
Retorna informações detalhadas sobre um bot do Discord com base no token fornecido.

---

### **Requisição**

**URL:** `POST /bot/info`

**Body (JSON):**
```json
{
  "token": "SeuTokenAqui"
}
```

---

### **Respostas**

#### Sucesso (200):
```json
{
  "id": "123456789",
  "username": "BotName",
  "discriminator": "1234",
  "avatar": "https://cdn.discordapp.com/avatars/123456789/avatar.png",
  "bot": true
}
```

#### Erros:
| Código | Mensagem                         |
|--------|----------------------------------|
| 400    | O campo "token" é obrigatório. |
| 401    | Token inválido.                 |
| 429    | Rate limit excedido.            |

---

### **Exemplo de Uso**

```bash
curl -X POST https://urldaapi/bot/info \
-H "Content-Type: application/json" \
-d '{"token":"SeuTokenAqui"}'
```
