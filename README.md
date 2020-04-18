# Emmet

- Es un plugin para editores de texto para mejores el flujo de trabajo con HTML y CSS. 
- Emmet está integrado en Visual Studio Code, no se requiere instalar una extensión.

## HTML 

### Estructura básica archivo HTML

 	! + tab

### Construcción de elementos simples

 
 Autocompletar etiqueta + inner Text
 
 	h1{Hola PlatziMasters} + tab
 	
 	<h1>Hola PlatziMasters</h1>
 
Div con id

	#main + tab
	
	<div id="main"></div>
	
Etiqueta con id

	img#logo
	
	<img src="" alt="" id="logo">	
	
Etiqueta con id y clase

	img#logo.big
	
	<img src="" alt="" id="logo" class="big">
	
Etiqueta con id y varias clases
		
	div#container.border.red
	
	<div id="container" class="border red"></div>

### Operador >


El operador `>` hace referencia a elementos hijo

Creación de elementos con elementos hijo
  
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
	    
Multiplicar elementos con texto


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

	div>ul>il{Calle $@150}*5
	
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



### Operador +
	
En caso de elementos en el mismo nivel se usa `+`

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

**Usando todos los shortcuts antes vistos**


Ejemplo de menu

	ul#menu>(li.nav>a:link>{Pagina $})*5
	
	<ul id="menu">
		<li class="nav"><a href="http://">Pagina 1</a></li>
		<li class="nav"><a href="http://">Pagina 2</a></li>
		<li class="nav"><a href="http://">Pagina 3</a></li>
		<li class="nav"><a href="http://">Pagina 4</a></li>
		<li class="nav"><a href="http://">Pagina 5</a></li>
	</ul>


Maquetación simple

	div#main-container>header+main+footer 
	
	<div id="main-container">
		<header></header>
		<main></main>
		<footer></footer>
	    </div>

Ejemplo estructura de un post

	(div.post>h2.title{Titulo}+span.date{yyyy-mm-dd}+div.content>lorem)*5
	
	<div class="post">
		<h2 class="title">Titulo</h2>
		<span class="date">yyyy-mm-dd</span>
		<div class="content">Lorem ipsum dolor, sit amet consectetur adipisicing elit. Laboriosam molestiae placeat nesciunt, provident et quasi maiores ducimus rerum. Dolore dicta doloremque laudantium dignissimos debitis at ipsum cum ut quidem? Rerum!</div>
	</div>
	
	
	
## ES7 React/Redux/GraphQL/React-Native snippets

### Que es un snippet?

Son pequeños fragmentos de código que pueden ser reusables en nuestros scripts. 

### React Components


React Component Class -> **rcc + tab**
	

	import React, { Component } from 'react'

	export default class Header extends Component {
	    render() {
		return (
		    <div>
		        
		    </div>
		)
	    }
	}


React Component Class -> **rce + tab**

	import React, { Component } from 'react'

	export class Header extends Component {
	    render() {
		return (
		    <div>
		        
		    </div>
		)
	    }
	}

	export default Header
	
	
Component Did Mount -> **cdm + tab**	

	componentDidMount() {
        
    	}

Component Will Unmount -> **cwu + tab**

	componentWillUnmount() {
	    
	}
		

React Pure Component -> **rpc + tab**

	import React, { PureComponent } from 'react'

	export default class Header extends PureComponent {
	    render() {
		return (
		    <div>
		        
		    </div>
		)
	    }
	}

React Pure Component -> **rpc + tab**

	import React, { PureComponent } from 'react'

	export class Header extends PureComponent {
	    render() {
		return (
		    <div>
		        
		    </div>
		)
	    }
	}

	export default Header

React Functional Component -> **rfc + tab**

	import React from 'react'

	export default function Header() {
	    return (
		<div>
		    
		</div>
	    )
	}

React Functional Component -> **rfe + tab**

	import React from 'react'

	function Header() {
	    return (
		<div>
		    
		</div>
	    )
	}

	export default Header


anonymous function -> **anfn + tab**
	   
	(params) => {
		
	    }

React component class with connected redux -> **rcredux +tab**

	import React, { Component } from 'react'
	import { connect } from 'react-redux'

	export class Header extends Component {
	    render() {
		return (
		    <div>
		        
		    </div>
		)
	    }
	}

	const mapStateToProps = (state) => ({
	    
	})

	const mapDispatchToProps = {
	    
	}

	export default connect(mapStateToProps, mapDispatchToProps)(Header)

	   
	    
## Emmet - JSX in VSCode

Configuar emmet para JSX

- Preferences + Settings + click in Open settings JSON
- También ctrl + shift + p -> Open settings JSON
- Incluir en el JSON de configuración


	"emmet.includeLanguages":{
		"javascript": "javascriptreact"
	}
	

- `ctrl + shift + p -> reload window`