<script>
	let logo = 'images/logo.svg';
	let cart = 'images/cart.svg';
</script>

	<header>
		<div class="logo-container">
		<img src={logo} alt="logo">
		<h4 class="logo">MacUI</h4>
		</div>
		<nav>
			<ul class="nav-links">
				<li><a class="nav-link" href="/">Home</a></li>
				<li><a class="nav-link" href="/">Specs</a></li>
				<li><a class="nav-link" href="/">Contact</a></li>
			</ul>
		</nav>
		<div class="cart">
			<img src={cart} alt="Cart">
		</div>
	</header>

	<main>
		<section class="hero">
			<div class="intro">
				<div class="intro-text">
					<h1>All your needs in one laptop</h1>
					<p>13.3 Inch with Retina Display</p>
				</div>
			
				<div class="cta">
					<button class="cta-select">13.3 Inch</button>
					<button class="cta-add">Add To Cart</button>
				</div>
			</div>
			<div class="cover">
				<img src="images/matebook.png" alt="Macbook">
			</div>
		</section>

		<img class="big" src="images/big-eclipse.svg" alt="bg">
		<img class="mid" src="images/mid-eclipse.svg" alt="bg">
		<img class="small" src="images/small-eclipse.svg" alt="bg">

		<div class="page-dots">
			<img src="images/arrow-left.svg" alt="prev">
			<img src="images/dot.svg" alt="">
			<img src="images/dot-full.svg" alt="">
			<img src="images/dot-full.svg" alt="">
			<img src="images/arrow-right.svg" alt="next">
		</div>
	</main>

<style>
	* {
		padding: 0;
		margin: 0;
		box-sizing: border-box;
	}

	header {
		display: flex;
		width: 80%;
		height: 10vh;
		margin: auto;
		align-items: center;
	}

	
	main {
		display: flex;
		text-align: center;
		padding: 1em;
		margin: auto;
		box-sizing: border-box;
	}

	.logo-container, 
	.nav-links,
	.cart img {
		display: flex;
	}

	.logo-container {
		flex: 1;
	}

	.logo {
		font-weight: 500;
		font-size: 18px;
		margin: 5px;
	}

	nav {
		flex: 2;
	}

	.nav-links {
		justify-content: space-around;
		list-style: none;
	}

	.nav-link {
		color: #999;
		font-size: 18px;
	}

	.nav-link:hover {
		color: black;
		text-decoration-line: none;
	}

	 .cart img {
		flex: 1;
		justify-content: flex-end;
	}

	.hero {
		display: flex;
		width: 90%;
		margin: auto;
		min-height: 80vh;
		align-items: center;
		align-content: center;
	}

	.intro {
		flex: 1;
	}

	.intro-text  h1{
		font-size: 44px;
		font-weight: 500;
		background: linear-gradient(to right, #494964, #6f6f89);
		-webkit-background-clip: text;
		-webkit-text-fill-color: transparent;
	}

	.intro-text p {
		margin: 5px;
		font-size: 22px;
		color: #999999;
	}

	.cta {
		padding: 50px 0 0 0;
	}

	.cta button:hover {
		box-shadow: 3px 10px 20px rgba(0,0,0,.3);
    	transform: translateY(-3px);
	}

	.cta-select {
		border: 2px solid lightblue;
		background: transparent;
		color: lightblue;
		width: 150px;
		height: 50px;
		cursor: pointer;
		font-size: 1rem;
	}

	.cta-add {
		background: lightblue;
		width: 150px;
		height: 50px;
		cursor: pointer;
		font-size: 1rem;
		color: #fff;
		border: none;
	}

	.cover {
		flex: 1;
	}

	.cover img {
		height: 60vh;
		filter: drop-shadow(0px 5px 3px black);
		animation: drop 1.5s ease;
	}

	.big {
		position: absolute;
		top: 0;
		right: 0;
		z-index: -1;
		opacity: 0.4;
		height: 60%;
	}

	.mid {
		position: absolute;
		top: 30;
		right: 30;
		z-index: -1;
		opacity: 0.7;
		height: 60%;
	}

	.small {
		position: absolute;
		bottom: 0;
		left: 20%;
		z-index: -1;
		height: 60%;
	}

	.page-dots {
		width: 18%;
		justify-content: space-around;
		display: flex;
		position: absolute;
		right: 20%;
		bottom: 3rem;
	}

	@keyframes drop {
		0% {
			opacity: 0;
			transform: translateY(80px);
		}

		100% {
			opacity: 1;
			transform: translateY(0);
		}
	}

	@media screen and (max-width: 1024px) {
		.hero {
			flex-direction: column;
		}

		.intro {
			margin-top: 5vh;
			text-align: center;
		}

		.intro-text h1 {
			font-size: 30px;
		}

		.intro-text p {
			font-size: 1.1rem;
		}

		.page-dots {
			bottom: 5%;
			right: 50%;
			width: 50%;
			transform: translate(50%, 5%);
		}

		.cover img {
			height: 80%;
		}

		.small, .mid, .big {
			opacity: .2;
		}
	}

</style>