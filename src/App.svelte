<script>
	import Router from 'svelte-spa-router'
	import Convite from './Convite.svelte'
	import Header from './Header.svelte'
//	import Footer from './Footer.svelte'
	import Home from './Home.svelte'

	const routes = {
			'/': Home,
			'/convite': Convite,
			}
	</script>
	
	<main> 
	
		<Header/>
	
		<div class="content">
			<Router routes={routes}/>
		</div>	

		<!-- //<Footer/> -->


	</main>

	<style>
		main{
			position:relative;
			overflow: hidden;
			max-width: 100%;
		}

	@media (min-width:991px){	
		main:after{
			content:"";
			position:absolute;
			background:var(--yellow);
			display: block;
			width:400px;
			height: 400px;
			top:40vh;
			right:0;
			z-index: 1;
			right: -200px;
			border-radius: 400px;
		}

		main:before{
			content:"";
			position:absolute;
			background-image: url("/assets/yellowtil.png");
			display: block;
			width:350px;
			height: 350px;
			top:90vh;
			left:0;
			z-index: 1;
			left: -200px;
			border-radius: 400px;
		}
	}
		.content{
			position:relative;
			z-index: 2;
		}
	</style>