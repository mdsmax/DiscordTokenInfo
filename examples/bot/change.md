## Endpoint: /change/update

### **Descrição:**
Atualiza propriedades do bot, como nome, descrição, ícone e banner.

---

### **Requisição**

**URL:** `POST /change/update`

**Body (JSON):**
```json
{
  "token": "SeuTokenAqui",
  "name": "Novo Nome",
  "description": "Nova descrição",
  "icon": "https://link-para-novo-icone.png",
  "banner": "https://link-para-novo-banner.png"
}
```

#### Sucesso (200):
```json
{
  "message": "Informações atualizadas com sucesso!",
  "data": {}
}
```

#### Erros:
| Código | Mensagem                          |
|--------|-----------------------------------|
| 400    | O campo "token" ou propriedades não fornecidas. |
| 401    | Token inválido.                  |
| 429    | Rate limit excedido.             |

---

### **Exemplo de Uso**

```bash
curl -X POST https://urldaapi/change/update \
-H "Content-Type: application/json" \
-d '{
  "token": "SeuTokenAqui",
  "name": "Novo Nome",
  "description": "Nova descrição",
  "icon": "https://link-para-novo-icone.png",
  "banner": "https://link-para-novo-banner.png"
}'
```
