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
	
		<Router routes={routes}/>


		<!-- //<Footer/> -->


	</main>
