<p align="center">
  <img src="https://zpaysolution.com/images/zpayabanner.png" alt="Z.PAY" width="100%" />
</p>

<p>
  <img
    align="left"
    src="https://i.pinimg.com/736x/40/c5/2d/40c52da2c014d773367ad145c627e949.jpg"
    alt="Gabriel Félix"
    width="140"
    height="140"
    style="border-radius: 9999px; object-fit: cover;"
  />
  <img
    align="right"
    src="https://zpaysolution.com/images/zayladeitada.png"
    alt="Zayla"
    height="140"
  />
  <br/><br/><br/>
  &nbsp;&nbsp;&nbsp;<strong>feito por Gabriel Félix ("isnouu")</strong>
</p>
<br clear="all"/>


---

<p align="center">
  <img src="https://zpaysolution.com/images/zaylahappy.png" alt="Zayla" height="140" />
</p>

# Z.PAY

API Pix **sem mensalidade** — gera cobrança, confirma em segundos e credita no saldo. Feita pra streamers, lojas, bots e quem quer plugar Pix sem enrolação.

**Site:** [zpaysolution.com](https://zpaysolution.com/)  
**Docs ao vivo:** [zpaysolution.com/docs](https://zpaysolution.com/docs/)  
**Base da API:** `https://zpaysolution.com/api/v1`

---

## Guias

| Guia | O que cobre |
| --- | --- |
| [Como gerar pagamento](docs/gerar-pagamento.md) | `POST /payments` — QR, copia e cola |
| [Consultar / aprovar pagamento](docs/consultar-pagamento.md) | Status `pending` → `paid` |
| [Checkout hospedado](docs/checkout.md) | Link pronto pra pagar |
| [Webhooks](docs/webhooks.md) | Aviso quando o Pix cair |
| [Cashout (enviar Pix)](docs/cashout.md) | Saque via API |
| [Crypto](docs/crypto.md) | BTC, ETH, SOL e mais |
| [White e Black](docs/white-black.md) | Taxas e limites por perfil |

---

## Em poucas linhas

```bash
curl -sS -X POST "https://zpaysolution.com/api/v1/payments" \
  -H "client-id: zpk_..." \
  -H "client-secret: zsk_..." \
  -H "Content-Type: application/json" \
  -d '{"amount":20,"payerName":"Cliente","description":"Pedido #1"}'
```

Resposta traz `paymentId`, `copyPaste` e `qrCodeBase64`. Quando o Pix é pago, o valor líquido entra no saldo (menos a taxa do perfil).

<p align="center">
  <img src="https://zpaysolution.com/images/zaylaapontando.png" alt="Zayla apontando" height="120" />
</p>

## Contas

| | **White** | **Black** |
| --- | --- | --- |
| Cash-in | R$ 0,50 | 6% + R$ 1,50 |
| Cashout API | R$ 0,50 | R$ 1,50 |
| Ticket máx. cash-in | R$ 2.000 | R$ 500 |
| Ideal para | vendas, bots, SaaS | alto risco / adulto |

Detalhes: [White e Black](docs/white-black.md)

---

## Links rápidos

- [Entrar / criar conta](https://zpaysolution.com/login/)
- [Como funciona](https://zpaysolution.com/howwork/)
- [FAQ](https://zpaysolution.com/faq/)
- [Termos](https://zpaysolution.com/termos/)
- [Privacidade](https://zpaysolution.com/politica-de-privacidade/)
- [Discord](https://zpaysolution.com/)

<p align="center">
  <img src="https://zpaysolution.com/images/zaylacelular.png" alt="Zayla celular" height="130" />
</p>

---

<p align="center">
  <sub>Z.PAY Tecnologia · Pix, checkout, crypto e webhooks · <a href="https://zpaysolution.com/">zpaysolution.com</a></sub>
</p>
