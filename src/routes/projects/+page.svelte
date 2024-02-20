<script>
	import Project from '$lib/components/Project.svelte';
	import Github from '$lib/components/Github.svelte'

	let projects = [{
		name: 'Budgeteer',
		description: 'Budgeteer is next-gen budgeting that\'s easy to use yet powerful.',
		link: 'https://budgeteer.cc',
		icon: ''
	}, {
		name: 'Advance',
		description: 'Advance has been in development for two years, and I\'m happy to say it\'s now available to anyone who speaks English!',
		link: 'https://ds-advance.pages.dev',
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

<style>
	main {
		display: flex;
		flex-flow: column;
		align-items: center;
	}
</style>