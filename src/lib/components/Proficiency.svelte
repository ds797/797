<script>
	export let proficiency;
</script>

<main>
	{ #each Array(5) as _, i }
		<div class:first={i === 0} class:last={i === 4} class:highlighted={i < proficiency} />
	{ /each }
</main>

<style>
	main {
		display: flex;
		gap: 0.25rem;
	}

	div {
		width: 2rem;
		height: 0.5rem;
		background: var(--contrast-low);
	}

	.first {
		border-bottom-left-radius: 0.25rem;
		border-top-left-radius: 0.25rem;
	}

	.last {
		border-bottom-right-radius: 0.25rem;
		border-top-right-radius: 0.25rem;
	}

	.highlighted {
		background: var(--contrast);
	}
</style>