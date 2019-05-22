# Desafio Front-End

Nos útlimos anos o mercado de cursos online tem crescido exponencialmente nos cenários nacional e internacional. Com grandes players no mercado, como Hotmart, Udemy, Udacity, etc.., sejam eles produtores ou distribuidores de conteúdo, vê-se cada vez mais a necessidade de organizar e categorizar os cursos.

Sendo assim, o desafio consiste na criação de uma SPA, cujo objetivo é justamente fornecer ao consumidor final uma listagem categorizada de cursos disponíveis.

## SPA
Para isso, você deve desenvolver uma aplicação seguindo as seguintes normas:

###Tela de Login
Na tela de login `/login`, o usuário fornecerá as seguintes credenciais para acesso, tendo como resposta um JSON com as respectivas categorias e cursos existentes.
- `login: admin`
- `password: 12345678`
- Obs: Qualquer outro valor será recusado.


#### Autenticação de usuário:

**Request - POST: https://afiliart.herokuapp.com/courses**
<br>
Headers:

```javascript
{
  Content-Type: application/json
}
```

Body:

```javascript
{
	login: 'admin',
	password: '12345678'
}
```

**Response**
Status: 200

```javascript
[{
	name: String,
	courses: [
		{
			name: String,
			price: Number,
			description: String,
			img: String
		}
	]
}]
```

### Home
Na `/home`, os cursos devem ser agrupados conforme a categoria que pertencem.
Cada curso deve ser exibido com as seguintes informações:
- Imagem
- Nome
- Preço `BRL`
Ao clicar em algum curso, o usuário deve ser redirecionado à página específica do curso selecionado.

### Página do Curso
Na página específica de cada curso `/home/:courseName`, devem ser exibidas todas as informações disponíveis do curso selecionado.
Além disso, é necessário implementar uma feature capaz de indicar os cursos relacionados com o selecionado.

### Menu de Navegação
Sua aplicação deve conter um menu de navegação simples.

## Requisitos
Sua API deve ser desenvolvida seguindo os seguintes requisitos:
- Linguagem: Javascript (Angular, ReactJS, VUE).
- Hospedagem: qualquer hospedagem de sua preferência (dica: existem serviços que disponibilizam planos gratuitos).
- A partir do momento que for feito o `FORK` desse repositório, o prazo de entrega do desafio é de 5 dias. O código deverá ser postado em seu GitHub e deverá conter um arquivo `readme.md` com as especificações do seu projeto.

## Diferenciais
- Campo de busca em que o usuário possa buscar por cursos existentes na plataforma.
- Filtro na `/home` para ordenar os cursos pelo menor preço.
