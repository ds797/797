<script>
	export let page = 0;

	let pages = ['About', 'Skills', 'Projects'];
</script>

<main>
	{ #each pages as title, index }
		<div class='container' on:click={() => page = index}>
			<h3 class='title'>{title}</h3>
			<div class="select" style="{page === index
				? 'width: 1rem; background: var(--contrast);'
				: 'width: 0.5rem; background: var(--contrast-low);'
			}" />
		</div>
	{ /each }
</main>

<style>
	main {
		padding: 2rem;
		display: flex;
		justify-content: center;
		align-items: center;
		gap: 1rem;
	}

	.container {
		display: flex;
		flex-flow: column;
		justify-content: center;
		align-items: center;
		gap: 0.5rem;
		cursor: pointer;
	}

	.title {
		color: var(--contrast);
	}

	.select {
		height: 0.5rem;
	}
</style>