<script>
	import { fade } from 'svelte/transition'
	import Navbar from '$lib/components/Navbar.svelte'
	import './styles.css'

	export let data
</script>

<main>
	<Navbar />
	<div class="page">
		{ #key data.pathname }
			<div class="content" in:fade={{ duration: 200, delay: 300 }} out:fade={{ duration: 300 }}>
				<slot />
			</div>
		{/key}
	</div>
</main>

<style>
	main {
		flex: 1;
		display: flex;
		flex-direction: column;
		width: 100%;
		margin: 0 auto;
		box-sizing: border-box;
	}

	.page {
		flex: 1;
	}

	.content {
		position: absolute;
		left: 0;
		right: 0;
		display: flex;
		flex-flow: column;
		align-items: center;
	}
</style>