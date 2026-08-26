# Checkout hospedado

<p align="center">
  <img src="https://zpaysolution.com/images/zaylacelular.png" alt="Zayla" height="120" />
</p>

← [Voltar ao README](../README.md)

Página com QR e copia e cola pronta. O cliente abre o link e paga. Expira em **30 minutos**.

## Endpoint

`POST https://zpaysolution.com/api/v1/checkout`  
(veja o payload exato em [docs](https://zpaysolution.com/docs/))

A resposta devolve a URL pública do checkout, no estilo:

`https://zpaysolution.com/checkout/...`

## O que o cliente vê

- Nome da loja / descrição do pedido  
- Valor  
- QR Code + Pix copia e cola  
- Contagem regressiva até expirar  

Ideal pra quem não quer montar tela de pagamento.

Também existe página de cobrança por usuário:

`https://zpaysolution.com/donate/seuusuario`

---

[Gerar pagamento via API](gerar-pagamento.md) · [Webhooks](webhooks.md)
