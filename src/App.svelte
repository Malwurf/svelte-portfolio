<script>
	import Navigation from './navigation/Navigation.svelte';
	import AboutPage from './pages/about/about.svelte'
	import ContactPage from './pages/contact/contact.svelte'
	import PortfolioPage from './pages/portfolio/portfolio.svelte'
	import StartPage from './pages/start/start.svelte'
	import CvPage from './pages/cv/cv.svelte'
	import HobbyPage from './pages/hobby/hobby.svelte'
	
	
	let renderComponent = StartPage
</script>

<style lang="scss">
	.content {
		margin-left: 30px;
	}
</style>

<section>
	<Navigation
	    on:AboutPage={() => {renderComponent = AboutPage}}
		on:StartPage={() => {renderComponent = StartPage}}
		on:CvPage={() => {renderComponent = CvPage}}
		on:PortfolioPage={() => {renderComponent = PortfolioPage}}
		on:HobbyPage={() => {renderComponent = HobbyPage}}
		on:ContactPage={() => {renderComponent = ContactPage}}/>
</section>

<section class="content">
	<svelte:component this={renderComponent}/>
</section>