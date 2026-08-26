# Cashout (enviar Pix)

<p align="center">
  <img src="https://zpaysolution.com/images/zaylacashoutpix.png" alt="Zayla cashout" height="120" />
</p>

← [Voltar ao README](../README.md)

Envia saldo da conta via Pix (chave ou copia e cola).

## Requisitos

- KYC verificado  
- Idade mínima **16 anos** (regra da plataforma)  
- Telefone verificado quando o painel exigir  

## Endpoint

`POST https://zpaysolution.com/api/v1/cashout`

Headers: `client-id` + `client-secret`.

Taxa típica:

- **White:** R$ 0,50 por envio  
- **Black:** R$ 1,50 por envio  

Saque pelo painel também funciona (mínimos e taxas podem diferir — confira o FAQ atual).

---

[White e Black](white-black.md) · [Docs](https://zpaysolution.com/docs/)
