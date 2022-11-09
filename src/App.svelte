<script>
	import Navigation from './Navigation.svelte';
	import About from './pages/About.svelte';
	import Skills from './pages/Skills.svelte';
	import Projects from './pages/Projects.svelte';

	let page = 0;
</script>

<main>
	<Navigation bind:page />
	<About />
	<Skills />
	<Projects />
</main>

<style>

</style>