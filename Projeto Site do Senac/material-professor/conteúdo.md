## Guia para a primeira aula prática com o projeto do site senac

<br/>

### Começamos reconhecendo o código

<br/>


### Vamos criar o reset

1. Criar a pasta estilos.
2. Explicar a necessidade de um arquivo reset e criar o 'reset.css'.
3. Usando a estratégia de agrupamento, zerar todas as configurações de margem, preenchimento, borda, e estabilizar o fon-size e font, e alinhar na vertical.
4. Primeiro tentem fazer pensando o jeito mais intuitivo, depois apresenta isso:

```css
*:after,
*:before {
	margin: 0;
	padding: 0;
	box-sizing: border-box;
	text-decoration: none;
}

body{
	font-size: 100%;
	list-style-type: none;
}
```

#### Explicando os seletores `*:after, *:before*`

Os seletores `*:after` e `*:before` aplicam-se a todos os elementos (`*` significa "todos os elementos"), e o `:after` e `:before` referem-se aos pseudo-elementos `::after` e `::before`, respectivamente.

- `::before`: Insere conteúdo **antes** do conteúdo real de um elemento.
- `::after`: Insere conteúdo **depois** do conteúdo real de um elemento.

Esses pseudo-elementos permitem adicionar algo antes ou depois de um elemento sem alterar diretamente o HTML.

No nosso código estamos aplicando um conjunto de estilos padrão para todos os pseudo-elementos `::after` e `::before` em todos os elementos da página. 

**Exemplo do uso de `::before` e `::after`?****

Esses pseudo-elementos são usados principalmente para adicionar elementos decorativos ou funcionais sem inserir novos elementos HTML, o que pode manter o código mais limpo.

Por exemplo, vamos inserir uma estrela antes de cada botão.:

```css
button::before {
    content: "⭐"; /* Insere uma estrela antes do conteúdo do botão */
}
```

----

### Vamos criar as classes para os nossos elementos!

Não vamos poder seguir o que o Prof. Miguel fez porque ele usou um monte de div. Quero reforçar com os estudantes o uso de lementos semânticos.

1. Vamos analisar o objetivo final para a página home e bolar uma estratégia. Vamos focar só na página home por enquanto.
	1. Quais são os elementos estilizados?
	2. O que caracteriza cada um deles?
	3. Vamos pensar quais atributos CSS podemos nobilizar para alcançar cada um desses objetivos.

Aqui está o resultado final que eu fiz:


Aqui está a dica de como o professor fez:

```html
<!DOCTYPE HTML>
<html lang="pt-br">
	<head>
		<title>Programa Senac Gratuidade</title>
		<meta charset="UTF-8" />
		<link rel="shortcut icon" 
		type="image/x-icon" 
		href="./img/favicon.ico" />
		<link rel="stylesheet" type="text/css" 
		href="./css/estilo.css"	/>
		<link rel="stylesheet" type="text/css" 
		href="./css/layout.css"	/>
		<link rel="stylesheet" type="text/css" 
		href="./css/reset.css"	/>
	</head>
<body>
<div id="corpo"><!--Inicio div corpo -->
	<div id="cabecalho"><!--Inicio div cabecalho -->
		<div id="cabelhoEsq"><!--Inicio div cabelhoEsq -->
			<p class="p1">
			<a href="./index.html">
			<img src="./img/senac_logo_new.png" 
			alt="Logotipo SenacRS" 
			title="Logotipo SenacRS" />
			</a>
			</p>
		</div><!--Fim div cabelhoEsq -->
		<div id="cabecalhoMeio"><!--Inicio div cabecalhoMeio -->
			<!--mudança do id da tag p -->
			<p id="pCabecalhoMeio">Rio Grande do Sul</p>
		</div><!--Fim div cabecalhoMeio -->
		<div id="cabecalhoDir"><!--Inicio div cabecalhoDir -->
			<!--mudança do id da tag p -->
			<p id="plink">
			<a class="linkRedes "href="https://www.facebook.com/senacrsoficial" target="blank">
			<img class="imgRedes" src="./img/icon_facebook.png" 
			alt="Rede social Facebook" 
			title="Rede social Facebook"/>
			</a>
			<a class="linkRedes href="https://www.instagram.com/senacrs/" target="blank">
			<img class="imgRedes" src="./img/icon_instagram.png" 
			alt="Rede social Instagram" 
			title="Rede social Instagram" />
			</a>
			<a class="linkRedes href="https://x.com/senacrs" target="blank">
			<img class="imgRedes" src="./img/icon_twitter.png" 
			alt="Rede social X-Twitter" 
			title="Rede social X-Twitter" />
			</a>
			<a class="linkRedes href="https://www.linkedin.com/authwall?trk=gf&trkInfo=AQGjNOZytbRLdwAAAZCDGdKQorc6a1HY6F3qjme8z6BVRLg3Kf_kVJ6e2WdIWIQaf8cRxOiTYKMz4bfZdnAKle3AQRelQP4NsP7sHBP37X7E5DOoOr4lQF2mPZUvO0avML2F1HE=&original_referer=https://www.senacrs.com.br/&sessionRedirect=https%3A%2F%2Fbr.linkedin.com%2Fschool%2Fsenac-rs%2F" target="blank">
			<img class="imgRedes" src="./img/icon_linkedin.png" 
			alt="Rede social Linkedin" 
			title="Rede social Linkedin" />
			</a>
			<a class="linkRedes href="https://www.youtube.com/senacrsoficial" target="blank">
			<img class="imgRedes" src="./img/icon_youtube.png" 
			alt="Canal Youtube" 
			title="Canal Youtube" />
			</a>
			<a class="linkRedes href="https://open.spotify.com/user/oe434380olmwip17xaxyjb0bc" target="blank">
			<img class="imgRedes" src="./img/icon_spotify.png" 
			alt="Canal Spotify" 
			title="Canal Spotify" />
			</a>
			</p>
		</div><!--Fim div cabecalhoDir -->
	</div><!--Fim div cabecalho -->
<hr class="hr1" />
<div id="divMenu"><!--Inicio divMenu -->
<!--Menu do sistema -->
<h1 id="h1">
<a href="./index.html">Home</a>|
<a href="./pages/oprograma.html">O programa</a>|
<a href="./pages/inscrever.html">Como se inscrever</a>|
<a href="./pages/consulta.html">Consulta de vagas</a>|
<a href="./pages/perguntas.html">Perguntas frequentes</a>|
<a href="./pages/fale_conosco.html">Fale Conosco</a>
</h1>
</div><!--Fim divMenu -->
<hr id="hr2" />
<div id="divMeio"><!--Inicio divMeio -->
	<div id="divMeioSuperior"><!--Inicio divMeioSuperior -->
<img id="imgBanner" src="./img/banner_programa.jpg"  
 alt="Banner Programa" 
title="Banner programa Senac gratuidade" />
	</div><!--Fim divMeioSuperior -->
	<div id="divMeioCentro"><!--Inicio divMeioCentro -->
<h1 class="h2">O programa Senac Gratuidade</h1>
<p class="pText">
O que é o PSG.
<!--Tag strong coloca texto em destaque -->
<br />
<!--Tag em coloca texto em itálico -->
Firmado em 22 de julho de 2008 entre o Ministério da Educação, o Ministério do Trabalho, o Ministério da Fazenda, a Confederação Nacional do Comércio de Bens, Serviços e Turismo - CNC e o Senac, e ratificado pelo Decreto nº 6.633, de 5 de novembro de 2008 , o Programa Senac de Gratuidade – PSG tem por objetivo garantir o acesso à educação profissional de qualidade para pessoas cuja renda familiar mensal per capita não ultrapasse dois salários mínimos.
<br />
Pelo acordo celebrado, o Senac investe, desde 2014, 66,67% de sua Receita Líquida de Contribuição nesse importante programa de educação inclusiva.
</p>
<p class="p1">
<img id="imgBannerPsg" src="./img/card_cursos.jpg"  
alt="Banner cursos gratuitos" 
title="Banner sobre os cursos gratuitos" />
</p>
<h2 id="h3">
Confira o vídeo da campanha 
<br />
"Tá de graça tá no Senac"
</h2>
<p class="p1">
<iframe id="iframeYoutube" src="https://www.youtube.com/embed/8G7WRCJ8VVM?si=elJatw36tYsK2fEf" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
</p>

<h1 class="h2">Veja se você pode se inscrever no PSG.</h1>
<p class="pText">
O Programa Senac de Gratuidade foi pensado como um instrumento de inclusão produtiva para brasileiros oriundos de família de baixa renda.
</p>
<p class="pJustify">
A renda familiar mensal per capita é calculada somando-se a renda bruta dos componentes do grupo familiar e dividindo-se pelo número de pessoas que formam esse grupo familiar.
</p>
<p class="pJustify">
Se o resultado for até 2 salários mínimos federais, o candidato poderá concorrer a uma vaga no PSG.
</p>
<p class="pJustify">
Grupo familiar – corresponde ao próprio candidato e as pessoas que moram com ele, que usufruam da renda bruta familiar e tenham com o candidato algum grau de parentesco: pai, padrastro, mãe, madrastra, cônjuge, companheiro(a), filho(a), enteado(a), irmão(ã), ou avô(ó).
</p>
	</div><!--fim divMeioCentro -->
</div><!--Fim divMeio -->
<div id="divMenuFooter"><!--Inicio divMenuFooter -->
<hr class="hr1"/>

<h2 id="h2">
<a href="./index.html">Home</a>|
<a href="./pages/oprograma.html">O programa</a>|
<a href="./pages/inscrever.html">Como se inscrever</a>|
<a href="./pages/consulta.html">Consulta de vagas</a>|
<a href="./pages/perguntas.html">Perguntas frequentes</a>|
<a href="./pages/fale_conosco.html">Fale Conosco</a>
</h2>
</div><!--Fim divMenuFooter -->
<hr class="hr1" />
<div id="divFooter"><!--Inicio divFooter -->
<p class="p1">
<img src="./img/senac_logo_new.png" 
alt="Logotipo Senac" title="logotipo Senac">
</p>
<p class="p1">
<a class="linkRedes href="https://www.facebook.com/senacrsoficial" target="blank">
<img class="imgRedes" src="./img/icon_facebook.png" 
alt="Rede social Facebook" 
title="Rede social Facebook" />
</a>
<a class="linkRedes href="https://www.instagram.com/senacrs/" target="blank">
<img class="imgRedes" src="./img/icon_instagram.png" 
alt="Rede social Instagram" 
title="Rede social Instagram" />
</a>
<a class="linkRedes href="https://x.com/senacrs" target="blank">
<img class="imgRedes" src="./img/icon_twitter.png" 
alt="Rede social X-Twitter" 
title="Rede social X-Twitter" />
</a>
<a class="linkRedes href="https://www.linkedin.com/authwall?trk=gf&trkInfo=AQGjNOZytbRLdwAAAZCDGdKQorc6a1HY6F3qjme8z6BVRLg3Kf_kVJ6e2WdIWIQaf8cRxOiTYKMz4bfZdnAKle3AQRelQP4NsP7sHBP37X7E5DOoOr4lQF2mPZUvO0avML2F1HE=&original_referer=https://www.senacrs.com.br/&sessionRedirect=https%3A%2F%2Fbr.linkedin.com%2Fschool%2Fsenac-rs%2F" target="blank">
<img class="imgRedes" src="./img/icon_linkedin.png" 
alt="Rede social Linkedin" 
title="Rede social Linkedin" />
</a>
<a class="linkRedes href="https://www.youtube.com/senacrsoficial" target="blank">
<img class="imgRedes" src="./img/icon_youtube.png" 
alt="Canal Youtube" 
title="Canal Youtube" />
</a>
<a class="linkRedes href="https://open.spotify.com/user/oe434380olmwip17xaxyjb0bc" target="blank">
<img class="imgRedes" src="./img/icon_spotify.png" 
alt="Canal Spotify" 
title="Canal Spotify" />
</a>
</p>
<p id="pDireitos">
© Todos os Direitos Reservados - 2024.
</p>
	</div><!--Fim divFooter -->
</div><!--Fim div corpo -->
</body>	
</html>
```


```css
body{
	//background-image:url("../img/fundo.jpg");
	//background-color: red;
	//background-color: #00FFFF;
}
.p1{
	text-align: center;
	
}
.imgRedes{
	margin-left: 5px;
}
.linkRedes{
	text-decoration: none;
}
.hr1{
	background-color: #ffa500;
	height: 5px;
	border-radius: 4px;
	border: none;
	
}
#hr2{
	background-color: #ffa500;
	height: 5px;
	border-radius: 4px;
	border: none;
	margin-bottom: 0;
}
#h1{
	text-align: center;
}
#h2{
	text-align: center;
}
#imgBanner{
	width: 100%;
	height: auto;
	
}
.h2{
	text-align: center;
	font-family: arial black;
	font-size: 26px;
	margin-top: 1%;
	margin-bottom: 1%;
}
.pText{
	text-align: center;
	font-family: arial;
	font-size: 14px;
	margin-top: 1%;
	margin-bottom: 1%;
	margin-left: 1%;
	margin-right: 1%;
	line-height: 130%;
}
#imgBannerPsg{
	width: 80%;
	height: auto;
	border-radius: 4px;
}
#h3{
	text-align: center;
	font-family: arial;
	font-size: 20px;
	margin-top: 1%;
	margin-bottom: 1%;
	line-height: 130%;
}
#iframeYoutube{
	width: 560px;
	height: 315px;	
}
.pJustify{
	text-align: justify;
	font-family: arial;
	font-size: 14px;
	margin-top: 1%;
	margin-bottom: 1%;
	margin-left: 1%;
	margin-right: 1%;
	line-height: 130%;
}
#pDireitos{
	text-align: center;
	font-family: arial;
	font-size: 14px;
	margin-top: 2%;
	padding-bottom: 3%;
}
/*Código página oprograma.html*/
#imgAprendiz{
	width: 19%;
	height: auto;
	float: right;
	margin-left: 10px;
	margin-bottom: 10px;
}
/*Código página inscrever.html*/
#imgBannerInscricao{
	width: 80%;
	height: auto;
	border-radius: 4px;
}
#iframeMaps{
	width: 600px;
	height: 450px;
	border: 0;	 
}
/*Código página perguntas.html*/
#imgBannerPerguntas{
	width: 80%;
	height: auto;
	border-radius: 4px;
}
.hLeft{
	text-align: left;
	font-family: arial;
	font-size: 20px;
	margin-top: 1%;
	margin-bottom: 1%;
	margin-left: 1%;
	margin-right: 1%;
	line-height: 130%;
}
.liPerguntas{
	
	font-family: arial;
	font-size: 14px;
	margin-top: 1%;
	margin-bottom: 1%;
	margin-left: 5%;
	margin-right: 5%;
	line-height: 130%;
}
.ulPerguntas{
	list-style-type: square;
}
.olPerguntas{
	list-style-type: lower-alpha;
}
#olPerguntasSub{
	list-style-type: upper-roman;
	margin-left: 2%;
}
/*
Novos recursos de formatação, por conta do layout
Mudança nas tags p do cabeçalho
*/
#plink{
	text-align: right;
	margin-top: 5%;
	margin-bottom: 5%;
	margin-right: 10%;
}
#pCabecalhoMeio{
	text-align: center;
	margin-top: 5%;
	margin-bottom: 5%;
	font-family: arial black;
	font-size: 24px;
}
/*
Novos recursos de formatação, aula 18, por conta do layout
Mudança nas tags hr no corpo
*/
.hr2{
	background-color: #ffa500;
	width: 70%;
	height: 5px;
	text-align: center;
	text-align: center;
	border-radius: 4px;
	border: none;
	
}
#hr3{
	background-color: #0000CD;
	height: 5px;
	border-radius: 4px;
	border: none;
	margin-top: 4%;
	
}
#hr4{
	background-color: #0000CD;
	height: 5px;
	border-radius: 4px;
	border: none;
	margin-bottom: 0;
}
/*Formatação da página consulta na tabela */
.h3Td{
	font-family: arial;
	color: blue;
}
.imgCursos{
	width: 300px;
	height: auto;
}
/*Formatação do fale conosco */
#formP{
	font-size: 30px;
	text-align: center;
	font-weight: bold;
}
.dados{
	margin-bottom: 15px;
}
.dados label{
	font-family: arial black;
	font-size: 16px;
	margin-bottom: 5px;
	color: #666;
	display: block;
	
}
```