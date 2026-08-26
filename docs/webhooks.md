# Webhooks

<p align="center">
  <img src="https://zpaysolution.com/images/zaylacomofunciona.png" alt="Zayla" height="120" />
</p>

← [Voltar ao README](../README.md)

Receba um POST na sua URL quando Pix, checkout ou crypto for criado, pago, expirar ou falhar.

## Cadastro

No painel → aba **Webhooks** → cadastre até **5 URLs**.

Eventos comuns:

- `payment.created` / `payment.paid` / `payment.expired` / `payment.failed`
- `checkout.*`
- `crypto.*`

## Boas práticas

1. Responda **2xx** rápido.  
2. Idempotência: o mesmo evento pode chegar de novo (retry).  
3. Confirme o status com `GET /payments/{id}` se precisar de garantia extra.  
4. Guarde o `paymentId` / `transactionId` no seu banco.

Latência média de entrega citada no site: ~**50ms**.

---

Docs: [zpaysolution.com/docs/#webhooks](https://zpaysolution.com/docs/)
