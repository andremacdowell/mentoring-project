# mentoring-project
Mentoring Project

## Checkout API simple contract

```
POST api/v1.0/checkout
{
	"customer": {
		"first_name": "andre",
		"last_name": "macdowell",
		"email": "ab@cd.com",
		"contact_phone": "+55 21 99999-9999"
	},
	"delivery_address": {
		"address_line_1": "",
		"address_line_2": "",
		"state": "",
		"country": "",
		"zip_code": ""
	},
	"cart": {
		"items": [
			{
				"name": "item1",
				"cost": 9.99
			}
		]
	},
	"payment_information": {
		"card_brand": "mastercard",
		"card_number": "124123213213213",
		"card_security_code": "123",
		"expiration_date": "05/21"
	}
}
```

## Challenges
pagina web checkout - híbrida (stencil/svelte/react)
app checkout (android)
app checkout (ios)
pagina web checkout - pura (web components)
página web checkout + pwa (evolução web components c/ polymer)

1) endpoint de checkout simples na api flask 
	=> se ok, responde 201 - checkout realizado!
	=> se não ok, responde 400 - dizendo o que faltou


2) pagina web checkout - híbrida (stencil/svelte/react)
	=> implementar no framework de escolha o checkout para as informações que o endpoint de checkout espera
	=> tudo mockado, exceto os dados de pagamento
	=> validações no front-end para os campos obrigatórios
	=> responsivo


3) ou evolui na lista de opções de front-end/app
	ou evolui na modelagem e nas opções de escrita do back-end

## Checkout API evolution

```
GET api/v1.0/cart/<cart_id>

POST api/v1.0/cart
{
	items: [
		{
			"name": "Segredos da mente milionaria"
		}
	],
	customer_id: 123
}

PATCH api/v1.0/cart
{
	item: {
		"name": "Direito Concorrencial"
	},
	customer_id: 123	
}
```