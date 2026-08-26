# Como gerar pagamento

<p align="center">
  <img src="https://zpaysolution.com/images/zaylaapontando.png" alt="Zayla" height="120" />
</p>

← [Voltar ao README](../README.md)

Gera uma cobrança Pix com QR Code e copia e cola.

## Endpoint

`POST https://zpaysolution.com/api/v1/payments`

### Headers

```
client-id: zpk_...
client-secret: zsk_...
Content-Type: application/json
```

As chaves ficam na aba **API** do [painel](https://zpaysolution.com/). O `client-secret` só aparece uma vez.

### Body

```json
{
  "amount": 20.0,
  "payerName": "Cliente",
  "description": "Pedido #1234",
  "tag": "loja"
}
```

| Campo | Obrigatório | Notas |
| --- | --- | --- |
| `amount` | sim | BRL, mínimo **R$ 2,00** |
| `payerName` | sim | Nome exibido no Pix |
| `description` | não | Texto da cobrança |
| `tag` | não | Liga o pagamento a uma tag do painel |

### Exemplo (curl)

```bash
curl -sS -X POST "https://zpaysolution.com/api/v1/payments" \
  -H "client-id: zpk_SEU_ID" \
  -H "client-secret: zsk_SEU_SECRET" \
  -H "Content-Type: application/json" \
  -d "{\"amount\":20,\"payerName\":\"Cliente\",\"description\":\"Pedido #1\"}"
```

### Resposta (resumo)

```json
{
  "paymentId": "...",
  "copyPaste": "00020126...",
  "qrCodeBase64": "data:image/png;base64,...",
  "amount": 20,
  "status": "pending"
}
```

Mostre o QR / copia e cola pro cliente. Depois: [consultar ou aprovar](consultar-pagamento.md).

---

Docs oficiais: [zpaysolution.com/docs](https://zpaysolution.com/docs/)
