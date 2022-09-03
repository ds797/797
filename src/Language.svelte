<script>
	import Proficiency from './Proficiency.svelte';
	export let language;
</script>

<main>
	<div class="main">
		<img src={language.icon} alt="" />
		<div class="data">
			<h1>{language.name}</h1>
			<Proficiency proficiency={language.proficiency} />
		</div>
	</div>
	<div class="children">
		{ #each language.children ?? [] as language }
			<svelte:self {language} />
		{ /each }
	</div>
</main>

<style>
	main {
		display: flex;
		flex-flow: column;
		justify-content: center;
		gap: 3rem;
	}

	.main {
		width: 25rem;
		display: flex;
		align-items: center;
		gap: 1rem;
	}

	h1 {
		text-align: start;
	}

	.data {
		display: flex;
		flex-flow: column;
		justify-content: center;
		gap: 0.25rem;
	}

	.children {
		padding-left: 3rem;
	}

	img {
		width: 4rem;
		height: 4rem;
		border-radius: 0.5rem;
	}
</style>