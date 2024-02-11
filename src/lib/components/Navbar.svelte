<script>
	import { page } from '$app/stores'
	import { goto } from '$app/navigation'
</script>

<main>
	<button on:click={() => goto('/')}>
		<h3 class='title'>About</h3>
		<div class="select" style="{$page.url.pathname === '/'
			? 'width: 1rem; background: var(--contrast);'
			: 'width: 0.5rem; background: var(--contrast-low);'
		}" />
	</button>
	<button on:click={() => goto('/skills')}>
		<h3 class='title'>Skills</h3>
		<div class="select" style="{$page.url.pathname === '/skills'
			? 'width: 1rem; background: var(--contrast);'
			: 'width: 0.5rem; background: var(--contrast-low);'
		}" />
	</button>
	<button on:click={() => goto('/projects')}>
		<h3 class='title'>Projects</h3>
		<div class="select" style="{$page.url.pathname === '/projects'
			? 'width: 1rem; background: var(--contrast);'
			: 'width: 0.5rem; background: var(--contrast-low);'
		}" />
	</button>
</main>

<style>
	main {
		padding: 2rem;
		display: flex;
		justify-content: center;
		align-items: center;
		gap: 1rem;
	}

	button {
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