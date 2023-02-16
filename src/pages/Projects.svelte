<script>
	import Project from './Project.svelte';

	let projects = [{
		name: 'Tasks',
		description: 'Tasks has been in development for two years, and I\'m happy to say it\'s now available to everyone in America!',
		link: 'https://tasks-dnl.pages.dev/tasks',
		icon: ''
	}, {
		name: 'dst',
		description: 'dst is my math tutoring "agency". The website just contains information relating to the service.',
		link: 'https://dstutor.pages.dev',
		icon: ''
	}, {
		name: 'ds-os',
		description: 'ds-os is under construction. Progress is going great, but the project won\'t be publicly available until it reaches a more stable state.',
		link: '',
		icon: ''
	}];
</script>

<main>
	{ #each projects as project (project) }
		<Project {project} />
	{ /each }
</main>