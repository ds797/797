<script>
	import { page } from '$app/stores'
	import { goto } from '$app/navigation'
</script>

<main>
	<div class="left">

	</div>
	<div class="middle">
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
	</div>
	<div class="right">

	</div>
</main>

<style>
	main {
		padding: 1.5rem 1rem;
		display: flex;
		justify-content: stretch;
		align-items: stretch;
		gap: 1rem;
	}

	button {
		display: flex;
		flex-flow: column;
		justify-content: center;
		align-items: center;
		cursor: pointer;
	}

	.middle {
		flex: 2;
		display: flex;
		justify-content: center;
		align-items: center;
		gap: 0.5rem;
	}

	.left, .right {
		flex: 1;
		display: flex;
		justify-content: center;
		align-items: center;
	}

	.title {
		color: var(--contrast);
	}

	.select {
		height: 0.5rem;
	}
</style>