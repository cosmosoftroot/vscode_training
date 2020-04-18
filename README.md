# Emmet

## HTML shortcuts

Estructura básica archivo HTML

 	! + tab
 
 Autocompleta etiqueta + inner Text
 
 	div{hola} + tab
 	
 	<div>hola</div>
 
 
 Crear elementos con append childs
 
 
 	div>ul>li + tab
 	
	<div>
		<ul>
		    <li></li>
		</ul>
	</div> 
	
Multiplicar elementos


	div>ul>li*5
	
	<div>
		<ul>
		    <li></li>
		    <li></li>
		    <li></li>
		    <li></li>
		    <li></li>
		</ul>
	    </div> 
	    
Multiplicar elemento con texto


	div>ul>li{elemento}*5
	<div>
		<ul>
		    <li>elemento</li>
		    <li>elemento</li>
		    <li>elemento</li>
		    <li>elemento</li>
		    <li>elemento</li>
		</ul>
	    </div>	
	
Multiplicar elemento con texto + autoincremento

	div>ul>li{elemento: $}*5
	
	<div>
		<ul>
		    <li>elemento: 1</li>
		    <li>elemento: 2</li>
		    <li>elemento: 3</li>
		    <li>elemento: 4</li>
		    <li>elemento: 5</li>
		</ul>
	    </div>		
	
Multiplicar elemento con texto + autoincremento desde un número requerido

	div>ul>li>{Calle $@150}*6
	
	<div>
		<ul>
		    <li>
		        Calle 150
		        Calle 151
		        Calle 152
		        Calle 153
		        Calle 154
		        Calle 155
		    </li>
		</ul>
	    </div>

Capa con id

	#main + tab
	
	<div id="main"></div>
	
Etiqueta con id

	img#photo
	
	<img src="" alt="" id="photo">	
	
Etiqueta con id y clase

	img#photo.big
	
	<img src="" alt="" id="photo" class="big">
	
Etiqueta con id y varias clases

		
	div#container.border.red
	
	<div id="container" class="border red"></div>
	
El operador `>` hace referencia a operadores hijo, en caso de elementos en el mismo nivel se usa `+`


	div>img+div.header
	
	<div>
		<img src="" alt="">
		<div class="header"></div>
	    </div>

Agrupar elementos usando `()`


	div>(div.container>img.photo+div.titulo)*3
	
	<div>
		<div class="container">
		    <img src="" alt="" class="photo">
		    <div class="titulo"></div>
		</div>
		<div class="container">
		    <img src="" alt="" class="photo">
		    <div class="titulo"></div>
		</div>
		<div class="container">
		    <img src="" alt="" class="photo">
		    <div class="titulo"></div>
		</div>
	    </div>

Usando todos los shorcuts antes vistos

	div#main-container>header+main+footer 
	
	<div id="main-container">
		<header></header>
		<main></main>
		<footer></footer>
	    </div>

Ejemplo estructura de un post

	(div.post>h2.title+span.date+div.content>lorem)*5
	
	<div class="post">
		<h2 class="title"></h2>
		<span class="date"></span>
		<div class="content">Lorem, ipsum dolor sit amet consectetur adipisicing elit. Magnam iste architecto facere reprehenderit. Qui, commodi dicta obcaecati quod doloribus officiis error porro optio eum, doloremque repudiandae itaque nisi quasi natus.</div>
	    </div> ... * 5
	    
## JSX in VSCode

Configuar emmet para JSX

- Preferences + Settings + click in Open settings JSON
- También ctrl + shift + p -> escribir settings -> seleccionar Open settings JSON
- Incluir en JSON de configuración


	"emmet.includeLanguages":{
		"javascript": "javascriptreact"
	}

- `ctrl + shift + p -> reload window`