<script>
	import Navigation from './Navigation.svelte';
	import About from './pages/About.svelte';
	import Skills from './pages/Skills.svelte';
	import Projects from './pages/Projects.svelte';

	let page = 0;
</script>

<main>
	<Navigation bind:page />
	{ #if page === 0 }
		<About />
	{ :else if page === 1 }
		<Skills />
	{ :else if page === 2 }
		<Projects />
	{ :else }
		<h2>404</h2>
	{ /if }
</main>

<style>
	main {
		display: flex;
		flex-flow: column;
		justify-content: center;
		align-items: center;
	}
</style>