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
		<a href="https://github.com/ds797" target="_blank">GitHub</a>
		<svg xmlns="http://www.w3.org/2000/svg" width="1024" height="1024" viewBox="0 0 1024 1024" fill="none">
			<path fill-rule="evenodd" clip-rule="evenodd" d="M8 0C3.58 0 0 3.58 0 8C0 11.54 2.29 14.53 5.47 15.59C5.87 15.66 6.02 15.42 6.02 15.21C6.02 15.02 6.01 14.39 6.01 13.72C4 14.09 3.48 13.23 3.32 12.78C3.23 12.55 2.84 11.84 2.5 11.65C2.22 11.5 1.82 11.13 2.49 11.12C3.12 11.11 3.57 11.7 3.72 11.94C4.44 13.15 5.59 12.81 6.05 12.6C6.12 12.08 6.33 11.73 6.56 11.53C4.78 11.33 2.92 10.64 2.92 7.58C2.92 6.71 3.23 5.99 3.74 5.43C3.66 5.23 3.38 4.41 3.82 3.31C3.82 3.31 4.49 3.1 6.02 4.13C6.66 3.95 7.34 3.86 8.02 3.86C8.7 3.86 9.38 3.95 10.02 4.13C11.55 3.09 12.22 3.31 12.22 3.31C12.66 4.41 12.38 5.23 12.3 5.43C12.81 5.99 13.12 6.7 13.12 7.58C13.12 10.65 11.25 11.33 9.47 11.53C9.76 11.78 10.01 12.26 10.01 13.01C10.01 14.08 10 14.94 10 15.21C10 15.42 10.15 15.67 10.55 15.59C13.71 14.53 16 11.53 16 8C16 3.58 12.42 0 8 0Z" transform="scale(64)" fill="var(--contrast-high)"/>
			<script xmlns="" id="bw-fido2-page-script"/>
		</svg>
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
		gap: 0.5rem;
	}

	.left {
		justify-content: flex-start;
	}

	.right {
		justify-content: flex-end;
	}

	.left svg, .right svg {
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