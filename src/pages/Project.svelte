<script>
  export let project;
</script>

<main>
	<a href={project.link} target='_blank'>
		<h2>{project.name}</h2>
	</a>
</main>

<style>
	a {
		text-decoration: solid underline var(--contrast) 0.125rem;
		text-underline-offset: 0.125rem;
	}
</style>