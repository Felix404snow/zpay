# Checkout hospedado

<p align="center">
  <img src="https://zpaysolution.com/images/zaylacelular.png" alt="Zayla" height="120" />
</p>

ÔåÉ [Voltar ao README](../README.md)

P├ígina com QR e copia e cola pronta. O cliente abre o link e paga. Expira em **30 minutos**.

## Endpoint

`POST https://zpaysolution.com/api/v1/checkout`  
(veja o payload exato em [docs](https://zpaysolution.com/docs/))

A resposta devolve a URL p├║blica do checkout, no estilo:

`https://zpaysolution.com/checkout/...`

## O que o cliente v├¬

- Nome da loja / descri├º├úo do pedido  
- Valor  
- QR Code + Pix copia e cola  
- Contagem regressiva at├® expirar  

Ideal pra quem n├úo quer montar tela de pagamento.

Tamb├®m existe p├ígina de cobran├ºa por usu├írio:

`https://zpaysolution.com/donate/seuusuario`

---

[Gerar pagamento via API](gerar-pagamento.md) ┬À [Webhooks](webhooks.md)
