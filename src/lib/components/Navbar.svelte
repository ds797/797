<script>
	import { page } from '$app/stores'
	import { goto } from '$app/navigation'
</script>

<main>
	<div class="left">
		<svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
			<path stroke-linecap="round" stroke-linejoin="round" d="M21.75 6.75v10.5a2.25 2.25 0 0 1-2.25 2.25h-15a2.25 2.25 0 0 1-2.25-2.25V6.75m19.5 0A2.25 2.25 0 0 0 19.5 4.5h-15a2.25 2.25 0 0 0-2.25 2.25m19.5 0v.243a2.25 2.25 0 0 1-1.07 1.916l-7.5 4.615a2.25 2.25 0 0 1-2.36 0L3.32 8.91a2.25 2.25 0 0 1-1.07-1.916V6.75" />
		</svg>
		<a href="mailto:ds797@duck.com">Get in touch</a>
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

	.left {
		justify-content: flex-start;
		gap: 0.5rem;
	}

	.left svg {
		width: 1.5rem;
		height: 1.5rem;
		color: var(--contrast-high);
	}

	.title {
		color: var(--contrast);
	}

	.select {
		height: 0.5rem;
	}
</style>