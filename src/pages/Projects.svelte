<script>
	import Project from './Project.svelte';

	let projects = [{
		name: 'Tasks',
		link: 'https://tasks-dnl.pages.dev',
		icon: ''
	}, {
		name: 'dst',
		link: 'https://dstutor.pages.dev',
		icon: ''
	}];
</script>

<main>
	{ #each projects as project (project) }
		<Project {project} />
	{ /each }
</main>