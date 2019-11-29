---
layout: default
---

# FreeMcBoot Configurator

**FreeMcBoot Configurator** is a tool for creating _FREEMCB.CNF_ files compatible with **Free McBoot**.

## ATTENTION!!!
----------------
**This software is experimental!**

I'm just a self-taught software developer and decided to start learning C#. :)

So please don't mind the badly designed spaghetti code. :P

# Images


<link rel="stylesheet" href="//netdna.bootstrapcdn.com/bootstrap/3.1.0/css/bootstrap.min.css">

<style>
		* {margin: 0; padding: 0;}
		body {background: #000}
		a,img {border: none;}
		.trs {-webkit-transition:all ease-out 0.5s;
			-moz-transition:all ease-out 0.5s;
			-o-transition:all ease-out 0.5s;
			-ms-transition:all ease-out 0.5s;
			transition:all ease-out 0.5s;}

		#slider {position: relative; z-index: 1;}
		#slider a { position: absolute; top: 0; left: 0; opacity: 0;filter:alpha(opacity=0);}
		.ativo {opacity: 1!important; filter:alpha(opacity=100)!important;}

		/*controladores*/
		span {background: #0190EE; cursor: pointer; opacity: 0;filter:alpha(opacity=0); position: absolute; bottom: 40%; width: 43px; height: 43px; z-index: 5;}
		.next {right: 10px;}
		.next:before,.next:after {left: 21px;}
		.next:before {
			-webkit-transform: rotate(-42deg);
			top: 5px;
		}
		.next:after {
			-webkit-transform: rotate(-132deg);
			top: 19px;
		}
		.next:before,.next:after,.prev:before,.prev:after {content: "";
			height: 20px;
			background: #fff;
			width: 1px;
			position: absolute;
		}
		.prev {left: 10px;}
		.prev:before,.prev:after {left: 18px;}
		.prev:before {
			-webkit-transform: rotate(42deg);
			top: 5px;
		}
		.prev:after {
			-webkit-transform: rotate(132deg);
			top: 19px;
		}
		figure:hover span {opacity: 0.76;filter:alpha(opacity=76);}
		figure {
			max-width: 937px;
			height: 354px;
			position: relative;
			overflow: hidden;
			margin: 50px auto;
		}
		figcaption {padding-left: 20px;color: #fff; font-family: "Kaushan Script","Lato","arial"; font-size: 22px; background: rgba(1, 144, 238, 0.76); width: 100%; position: absolute; bottom: 0; left: 0; line-height: 55px; height: 55px; z-index: 5}
	</style>

	<figure>
		<span class="trs next"></span>
		<span class="trs prev"></span>

		<div id="slider">
			<a href="#" class="trs"><img src="img/free-mcb-conf_01.jpg" alt="Legenda da imagem 1" /></a>
			<a href="#" class="trs"><img src="img/free-mcb-conf_02.jpg" alt="Legenda da imagem 2" /></a>
      <a href="#" class="trs"><img src="img/free-mcb-conf_03.jpg" alt="Legenda da imagem 3" /></a>
      <a href="#" class="trs"><img src="img/free-mcb-conf_04.jpg" alt="Legenda da imagem 4" /></a>
      <a href="#" class="trs"><img src="img/free-mcb-conf_05.jpg" alt="Legenda da imagem 5" /></a>		
		</div>

		<figcaption></figcaption>
	</figure>

	<script type="text/javascript">
		function setaImagem(){
			var settings = {
				primeiraImg: function(){
					elemento = document.querySelector("#slider a:first-child");
					elemento.classList.add("ativo");
					this.legenda(elemento);
				},
				slide: function(){
					elemento = document.querySelector(".ativo");
					if(elemento.nextElementSibling){
						elemento.nextElementSibling.classList.add("ativo");
						settings.legenda(elemento.nextElementSibling);
						elemento.classList.remove("ativo");
					}else{
						elemento.classList.remove("ativo");
						settings.primeiraImg();
					}
				},
				proximo: function(){
					clearInterval(intervalo);
					elemento = document.querySelector(".ativo");

					if(elemento.nextElementSibling){
						elemento.nextElementSibling.classList.add("ativo");
						settings.legenda(elemento.nextElementSibling);
						elemento.classList.remove("ativo");
					}else{
						elemento.classList.remove("ativo");
						settings.primeiraImg();
					}
					intervalo = setInterval(settings.slide,4000);
				},
				anterior: function(){
					clearInterval(intervalo);
					elemento = document.querySelector(".ativo");

					if(elemento.previousElementSibling){
						elemento.previousElementSibling.classList.add("ativo");
						settings.legenda(elemento.previousElementSibling);
						elemento.classList.remove("ativo");
					}else{
						elemento.classList.remove("ativo");						
						elemento = document.querySelector("a:last-child");
						elemento.classList.add("ativo");
						this.legenda(elemento);
					}
					intervalo = setInterval(settings.slide,4000);
				},
				legenda: function(obj){
					var legenda = obj.querySelector("img").getAttribute("alt");
					document.querySelector("figcaption").innerHTML = legenda;
				}
			}
			//chama o slide
			settings.primeiraImg();
			//chama a legenda
			settings.legenda(elemento);
			//chama o slide à um determinado tempo
			var intervalo = setInterval(settings.slide,4000);
			document.querySelector(".next").addEventListener("click",settings.proximo,false);
			document.querySelector(".prev").addEventListener("click",settings.anterior,false);
		}
		window.addEventListener("load",setaImagem,false);
	</script>


#### Official page:

* [FreeMcBoot Configurator - GitHub](https://github.com/AxionDrak/FreeMCBootConfigurator)

#### Download:

* [FreeMcBoot Configurator - ALPHA PREVIEW VERSION (NOT FUNCTIONAL!!!)](https://github.com/AxionDrak/FreeMCBootConfigurator/releases/tag/0.0.1.0)

## Hash
* * *
Use the table below to ensure that downloaded files do not change. These values are for files in their compiled (Alpha Preview) version.

| Filename                    | MD5                              | SHA256                                                           |
| --------------------------- | ---------------------------------|----------------------------------------------------------------- |
| LICENSE                     | e62637ea8a114355b985fd86c9ffbd6e | 230184f60bae2feaf244f10a8bac053c8ff33a183bcc365b4d8b876d2b7f4809 |
| FMCBootConfigurator_APV.exe | b8676883b2bd4ffc1fd19b1abeb4b9cc | b433ea04213383413ef96b965a9b48281b84a1ec4d4579e81a17bccd26faffe4 |
| README.md                   | 536643ae2f8e1ad86ccc731a3c8049ea | 6995ddc6e286be362ef6c819587d71e3d811f6d87532837f428bffbe72734a64 |

## Features
* * *
* Create FREEMCB.CNF file (for FREE McBoot) / under development. <b>NOT FUNCTIONAL!!!</b>

## Languages
* * *
* At the moment, only English is supported (sorry :/)

## Compile
* * *
See _COMPILE_ file for how to compile and install FreeMcBoot Configurator.

## Documentation
* * *
See _README_ for FreeMcBoot Configurator information.

## License
* * *
This project is released under the GNU license. If you redistribute the binary or source code of FreeMcBoot Configurator, please attach file _LICENSE_ with your products.
Review LICENSE file for further details.

* * *
Copyright 2019, Laete Meireles (a.k.a Axion Drak)

<<[back](./)
