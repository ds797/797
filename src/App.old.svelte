<script>
	import web from './assets/web.svg';
	import js from './assets/js.svg';
	import svelte from './assets/svelte.svg';
	import html from './assets/html.svg';
	import css from './assets/css.svg';
	import c from './assets/c.svg';
	import cpp from './assets/c++.svg';
	import nasm from './assets/nasm.svg';
	import python from './assets/python.svg';
	import Language from './Language.svelte';
	import Github from './Github.svelte';

	let languages = [{
		name: 'Web',
		icon: web,
		proficiency: 5,
		children: [{
			name: 'HTML',
			icon: html,
			proficiency: 5
		}, {
			name: 'CSS',
			icon: css,
			proficiency: 5
		}, {
			name: 'JavaScript',
			icon: js,
			proficiency: 5
		}, {
			name: 'Svelte',
			icon: svelte,
			proficiency: 5
		}]
	}, {
		name: 'C++',
		icon: cpp,
		proficiency: 4
	}, {
		name: 'C',
		icon: c,
		proficiency: 4
	}, {
		name: 'Assembly (NASM)',
		icon: nasm,
		proficiency: 4
	}, {
		name: 'Python',
		icon: python,
		proficiency: 3
	}];
</script>

<main>
	<h1>Hello! I'm ds797.</h1>
	<Github />
	{ #each languages as language (language) }
		<Language {language} />
	{ /each }
</main>

<style>
	main {
		padding: 2rem 8rem;
		display: flex;
		flex-flow: column;
		justify-content: center;
	}

	h1 {
		font-size: 4rem;
	}
</style>