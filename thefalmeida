<!DOCTYPE HTML>
<html>
	<head> 
		<title>Crypto World</title>
		<meta charset="utf-8" />
		<meta name="viewport" content="width=device-width, initial-scale=1, user-scalable=no" />
		<link rel="stylesheet" href="assets/css/main.css?v=7" />
		<noscript><link rel="stylesheet" href="assets/css/noscript.css" /></noscript>
		<link rel="icon" type="image/png" href="images/favicon.png">
	</head>
	<body class="landing is-preload">
 
		<!-- Page Wrapper -->
		<div id="page-wrapper">

			<!-- Header -->
				<header id="header" class="alt wrapper" >
					<div class="inner">
						<h1><a href="index.html"><img src="images/logo.png"></a></h1>
					<nav id="nav">
						<ul>
							<li class="special">
								<a href="#menu" class="menuToggle"><span>Menu</span></a>
								<div id="menu">
									<ul>
										<li><a href="#">Home</a></li>
										<li><a href="#">Nosotros</a></li>
										<li><a href="#">Servicios</a></li>
										<li><a href="#">Contacto</a></li>
										
									</ul>
								</div>
							</li>
						</ul>
					</nav>

					</div>
					
				</header>

			<!-- Banner -->
			<section id="banner">
				<div class="canvas-bg"></div>
				<div class="inner">
					<h2><img src="images/logo.png"></h2>
					<p>
						El futuro es digital</p>
				</div>
				<a href="#one" class="more scrolly">Conocenos</a>
			</section>

			<!-- One -->
				<section id="one" class="wrapper style1 special">
					<div class="inner">
						<header class="major">
							<h2>Nosotros<br /></h2>
							<p>
								Somos una academia que busca llevar el conocimiento del Mundo de las Criptomonedas, la Tecnologia Blockchain y las nuevas Finanzas Descentralizadas a cualquier persona que quiera capacitarse en este sector y aprovechar todas las oportunidades del futuro de la Economia Digital.<br>
							</p>
						</header>
						
					</div>
				</section>

			

			<!-- Three -->
				<section id="three" class="wrapper style3 special">
					<div class="inner">
						<header class="major">
							<h2>Servicios</h2>
							<p>Accede a nuestra academia y adquiere todo el conocimiento <br> para dedicarte profesionalmente a las criptomonedas.<br/> 
					</p>
						</header>
						<ul class="features">
							<li class="icon solid fa-graduation-cap">
								<h3>Academia Financiera</h3>
								<p>Contamos con cursos de formación de criptomonedas y trading.</p>
							</li>
							<li class="icon solid fa-laptop">
								<h3>Asesoría en Trading</h3>
								<p>Formación privada 100% personalizada en trading.</p>
							</li>
							<li class="icon solid fa-hand-holding-usd">
								<h3>Asesoramiento en Inversiones</h3>
								<p>Asesoramiento 100% personalizado en inversiones.</p>
							</li>
							<li class="icon solid fa-handshake">
								<h3>Compraventa de activos digitales</h3>
								<p>Gestion y ejecucion transparante de las operaciones.</p>
							</li>
						
						</ul>
					</div>
				</section>

			<!-- CTA -->
					<section id="contact" class="wrapper style4">
					<div class="inner">
						<div class="row">							
							<div class="col-8 col-12-xsmall" id="contact-form">
								<h2>Contacto</h2>
								<form method="post" action="#">
									<input type="text" placeholder="Nombre" required><br>
									<input type="text" placeholder="Email" required><br>
									<input type="text" placeholder="Whatsapp" required><br>
									<textarea placeholder="Mensaje" rows="6" required></textarea><br>
									<ul class="actions"> 
										<li><button class="special">Enviar</button></li>
									</ul>
									<div id="contact-form-alert"></div>
								</form>
								<script>
									document.addEventListener("DOMContentLoaded", function(event) {
										const token = 'e5cbb5d097f9aade7445fe21d522185791b8249975b17a53a6f3ed942c19dd97d46385652123442e44073d91b42deb5020f6cd71aa281e866b0d6983e6abe56008df5cfc69699cf959246773a9171d2ce8b303973038d9fd5bd38a9da9d2dd279562877de6dc7e7492f4d32b8ff86911ae01044ea44ba2ffc0731cc5e91c9688dab3ffa03f3d91099b778d55bbb9f30b06bb4f44cd2d632c23e6e8fa1196f6b9a22dec2e548e9193fe596d20b9704db59070c1735716384e60a4422d33fcaf016bb31d8ef8fcf10e573739f9bedbc5228b99699259eb6b91fb4a749f6de593d0a08b5a44cf760dcd74f11e582f2e7911ef7a9afd05b0bae8043b5e4df80fff0794279cd5290a530ebcf8f783c75be3275e88460510b6125dc70896a109d3dbfc330ef6eca33c5ddfbc923fdea1da91e89b0725af08a23edfb79ef1d3a4f410cc62ac65026da73600817802c0c3f94aec5b2ddb4a80c99a096f8c8af82bc0a987540d9db04df487828f2a1156174b933ef55277191753b0d870c9';

										var contacto = document.querySelector('#contact-form');

										contacto.querySelector('form button.special')
											.addEventListener('click', function(evt) {
												evt.preventDefault();

												var data = Array.prototype.slice.call(contacto.querySelectorAll('input, select, textarea'))
																				 .reduce(function(data, input) { data[input.getAttribute('placeholder')] = input.value; return data; }, {}),
														msg = contacto.querySelector('#contact-form-alert');

												msg.innerHTML = "";
												msg.classList.remove('error');
												msg.classList.remove('success');

												for (var key in data) {
													if (data[key].trim() === "") {
														msg.classList.add('error');
														msg.innerHTML = "Debe completar un " + key.toLowerCase() + " para enviar su consulta."
														return null;
													}
												}

												contacto.classList.add('loading');
												Proka.call("email", { email: { data: data }, token: token }, true)
													.then(function() {
														Array.prototype.slice.call(contacto.querySelectorAll('input, select, textarea'))
																	.forEach(function(input){ input.value = ""; });

														msg.classList.remove('error');
														msg.classList.add('success');
														msg.innerHTML = "Su consulta ha sido recibida, en breve nos comunicaremos con usted.";
													})
													.catch(function() {
														msg.classList.remove('success');
														msg.classList.add('error');
														msg.innerHTML = "Ocurrio un error, por favor intentelo nuevamente.";
													})
													.then(function() {
														contacto.classList.remove('loading');
													});
											});


									});
								</script>
							</div>
							<div class="col-4 col-12-xsmall">									
								<ul class="iconitos">									
									<li class="icon fa-map">
										<a href="https://goo.gl/maps/K9vwxNWMb5e4Bra38">
											<h3>Direccion</h3>
											<p>Rivadavia 15 Primer piso<br>Chivilcoy, Buenos Aires</p>
										</a>									
									</li>
									<li class="icon brands fa-whatsapp">
										<a href="https://api.whatsapp.com/send?phone=542346571268&text=Hola!%20Estoy%20interesado%20en%20los%20servicios%20que%20vi%20en%20su%20sitio%20web">
											<h3>Whatsapp</h3>
											<p>2346 - 571268</p>
										</a>
									</li>
									<li class="icon fa-envelope">
										<a href="mailto:info@cryptoword.com.ar">
											<h3>Email</h3>
											<p>info@cryptoword.com.ar</p>
										</a>
									</li>										
									<li class="icon brands fa-instagram">
										<a href="https://www.instagram.com/cryptoworld_arg/?hl=es">
											<h3>Instagram</h3>
											<p>@cryptoword_arg</p>
										</a>
									</li>									
								</ul>	
							</div>							
						</div>
					</div>						
				</section>
		</div>

		<!-- Scripts -->
		<script src="assets/js/jquery.min.js"></script>
		<script src="assets/js/jquery.scrollex.min.js"></script>
		<script src="assets/js/jquery.scrolly.min.js"></script>
		<script src="assets/js/browser.min.js"></script>
		<script src="assets/js/breakpoints.min.js"></script>
		<script src="assets/js/util.js"></script>
		<script src="assets/js/main.js"></script>
		<script src="assets/js/three.js"></script>
		<script src="assets/js/globe.js?v=2"></script>
		<script src="js/proka.js"></script>
	</body>
</html>
