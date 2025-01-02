### **Ativar Todas as Intents**

**URL:** `POST /bot/intents/activate`

**Body (JSON):**
```json
{
  "token": "SeuTokenAqui"
}
```

#### Sucesso (200):
```json
{
  "message": "Todas as intents foram ativadas com sucesso!",
  "data": {}
}
```

#### Erros:
| Código | Mensagem                         |
|--------|----------------------------------|
| 400    | O campo "token" é obrigatório. |
| 401    | Token inválido.                 |

---

### **Listar Intents**

**URL:** `POST /bot/intents/list`

**Body (JSON):**
```json
{
  "token": "SeuTokenAqui"
}
```

#### Sucesso (200):
```json
{
  "intents": {
    "GUILDS": true,
    "GUILD_MEMBERS": false,
    "GUILD_MESSAGES": true
  }
}
```

#### Erros:
| Código | Mensagem                         |
|--------|----------------------------------|
| 400    | O campo "token" é obrigatório. |
| 401    | Token inválido.                 |

---

### **Exemplo de Uso**

#### Ativar Todas as Intents:
```bash
curl -X POST https://urldaapi/bot/intents/activate \
-H "Content-Type: application/json" \
-d '{"token":"SeuTokenAqui"}'
```

#### Listar Intents:
```bash
curl -X POST https://urldaapi/bot/intents/list \
-H "Content-Type: application/json" \
-d '{"token":"SeuTokenAqui"}'
```
