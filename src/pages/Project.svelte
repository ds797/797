<script>
  export let project;
</script>

<main>
	{ #if project.link }
		<a href={project.link} target='_blank'>
			<h2>{project.name}</h2>
		</a>
		{ #if project.description }
			<p>{project.description}</p>
		{ /if }
	{ :else }
		<h2 class='unavailable'>{project.name} (unavailable)</h2>
		{ #if project.description }
			<p class='unavailable'>{project.description}</p>
		{ /if }
	{ /if }
</main>

<style>
	a {
		text-decoration: solid underline var(--contrast) 0.125rem;
		text-underline-offset: 0.125rem;
	}

	p {
		max-width: min(35rem, 90vw);
	}

	.unavailable {
		color: rgba(255, 0, 0, 0.8);
	}
</style>