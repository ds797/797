<script>
	import web from '../assets/web.svg';
	import js from '../assets/js.svg';
	import react from '../assets/react.svg';
	import svelte from '../assets/svelte.svg';
	import html from '../assets/html.svg';
	import css from '../assets/css.svg';
	import c from '../assets/c.svg';
	import cpp from '../assets/c++.svg';
	import nasm from '../assets/nasm.svg';
	import python from '../assets/python.svg';
	import Language from '../Language.svelte';

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
			name: 'React',
			icon: react,
			proficiency: 5
		}, {
			name: 'Svelte',
			icon: svelte,
			proficiency: 4
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
	<h3>Some categories can be expanded.</h3>
	{ #each languages as language (language) }
		<Language {language} />
	{ /each }
</main>

<style>
	main {
		width: min(35rem, 90vw);
		display: flex;
		flex-flow: column;
		justify-content: center;
		align-items: center;
		gap: 2rem;
	}


</style>