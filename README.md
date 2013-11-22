<h1>skewerRoute, crie rotas com geolocation!</h1>

<ul>
<li>Copyright (C) 2013, <a href="https://github.com/ralves87">Rafael Alves</a></li>
<li>Versão atual: 1.0</li>
</ul>

<p>Necessita do jQuery 1.9+</p>

<h2>Como usar</h2>

<p>O <code>skewerRoute</code> tem a finalidade de criar rotas automáticas a partir da geolocalização. Tendo a possibilidade de alterar temas, adicionar novas rotas e customizar os markers, tudo isso de uma maneira bem simples.</p>

<pre>
<script src="http://ajax.googleapis.com/ajax/libs/jquery/1.10.1/jquery.min.js" type="text/javascript"></ script>
<script src="core/skewerRoute.js" type="text/javascript"></ script>
</pre>

<pre>$(".skewerRoute").skewerRoute();</pre>

<h3>Configurações do mapa</h3>
<p>Veja como é fácil configurar o mapa com o <code>skewerRoute</code>.</p>

<pre>
$(".skewerRoute").skewerRoute({
	controls:{
		navigate: false, 	//Habilita o controle de navegação do mapa.
		zoom: false,		//Habilita o zoom.
		type: false,		//Habilita a opção de altarar o mapa para o modo satélite.
		scale: false,		//Habilita a escala do mapa.
		streetview: false,	//Habilita o streetview.
		overview: false,	//Habilita a visão global.
		scrollwheel: false	//Habilita zoom através do scroll do mouse.
	}
});
</pre>

<h3>Temas</h3>
<p>O nosso amigo <code>skewerRoute</code> possui alguns temas para você deixar o mapa mais atrente, veja o exemplo abaixo:</p>

<pre>
$(".skewerRoute").skewerRoute({
	theme: "BlackAndWhite"
});
</pre>

<p>Confira a lista atual de temas:</p>
<ul>
<li>BlackAndWhite</li>
<li>PaleDawn</li>
<li>Commander</li>
<li>BlueWater</li>
<li>BrightBubbly</li>
<li>NeutralBlue</li>
<li>Greyscale</li>
<li>VitaminC</li>
</ul>

<h3>Definindo a rota</h3>
<p>Para definir a localização do distino, basta preencher o parâmetro <code>route</code> com o endereço.</p>

<pre>
$(".skewerRoute").skewerRoute({
	route: "Campinas, SP"
});
</pre>

<h3>Makers</h3>
<p>O paramêtro <code>maker</code> é as imagens que representam o ponto incial e final. Os mesmos podem ser alterados através de imagens locais ou externas.</p>

<pre>
$(".skewerRoute").skewerRoute({
	marker: {
		pointA: "../path/pointA.png",	//Imagem para o ponto Geolocation.
		pointB: "../path/pointB.png",	//Imagem para o ponto de Destino.
		pointC: "../path/pointC.png"	//Imagem para o ponto de novas rotas.
	}
});
</pre>

<h3>Novas rotas</h3>
<p>O <code>newRoute</code> tem a função de exibir ao usuário a possibilidade de corrigir a sua localização ou então adicionar novos pontos de rota.</p>

<pre>
$(".skewerRoute").skewerRoute({
	newRoute:{
		active: true,	//Ativa a função
		showTime: 1000	//Tempo para a alerta exibir.
	}
});
</pre>
