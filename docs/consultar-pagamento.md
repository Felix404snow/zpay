# Consultar / aprovar pagamento

<p align="center">
  <img src="https://zpaysolution.com/images/zaylahappy.png" alt="Zayla" height="120" />
</p>

← [Voltar ao README](../README.md) · [Gerar pagamento](gerar-pagamento.md)

Depois de gerar a cobrança, confira se o Pix caiu e force a sincronização com o gateway se precisar.

## Consultar status

`GET https://zpaysolution.com/api/v1/payments/{paymentId}`

```bash
curl -sS "https://zpaysolution.com/api/v1/payments/SEU_PAYMENT_ID" \
  -H "client-id: zpk_..." \
  -H "client-secret: zsk_..."
```

Status possíveis: `pending`, `paid`, `failed`, `expired`.

## Aprovar / confirmar

`POST https://zpaysolution.com/api/v1/payments/{paymentId}/approve`

A API consulta o gateway de verdade. Se o Pix estiver pago, credita o valor líquido no saldo.

```bash
curl -sS -X POST "https://zpaysolution.com/api/v1/payments/SEU_PAYMENT_ID/approve" \
  -H "client-id: zpk_..." \
  -H "client-secret: zsk_..."
```

Dica: use [webhooks](webhooks.md) pra não ficar em polling.

---

Docs: [zpaysolution.com/docs](https://zpaysolution.com/docs/)
