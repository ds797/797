<script>
  export let project;
</script>

<main>
	{ #if project.link }
		<a href={project.link} target='_blank'>
			<div class="row">
				<h2>{project.name}</h2>
				<svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor">
					<path stroke-linecap="round" stroke-linejoin="round" d="M15.75 9V5.25A2.25 2.25 0 0 0 13.5 3h-6a2.25 2.25 0 0 0-2.25 2.25v13.5A2.25 2.25 0 0 0 7.5 21h6a2.25 2.25 0 0 0 2.25-2.25V15m3 0 3-3m0 0-3-3m3 3H9" />
				</svg>
			</div>
		</a>
		{ #if project.description }
			<p>{project.description}</p>
		{ /if }
	{ :else }
		<div class="row">
			<h2 class='unavailable'>{project.name}</h2>
			<svg class='unavailable' xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor">
				<path stroke-linecap="round" stroke-linejoin="round" d="M12 9v3.75m9-.75a9 9 0 1 1-18 0 9 9 0 0 1 18 0Zm-9 3.75h.008v.008H12v-.008Z" />
			</svg>
		</div>
		{ #if project.description }
			<p class='unavailable'>{project.description}</p>
		{ /if }
	{ /if }
</main>

<style>
	h2 {
		font-weight: 500;
		font-size: 1.25rem;
	}

	p {
		max-width: min(35rem, 90vw);
	}

	.row {
		display: flex;
		justify-content: center;
		align-items: center;
		gap: 0.25rem;
	}

	.row svg {
		width: 1.25rem;
		color: var(--contrast);
	}

	.unavailable, svg.unavailable {
		color: rgba(255, 0, 0, 0.8);
	}
</style>