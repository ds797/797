<svelte:head>
	<title>About</title>
	<meta name="description" content="About ds797" />
</svelte:head>

<main>
	<p class="banner">I'm currently taking a hiatus in development/maintenance of programming-related projects to focus on research. If something is broken, please contact me.</p>
	<h2>I'm ds797, a student, programmer, and designer.</h2>
	<p>I love deep-diving into subjects I don't know much about, then coming out the other side brimming with knowledge. The universe, nature, and technology are some of my favorite subjects!</p>
	<p>I'm very passionate about programming, I understand how it works and I see limitless potential. I enjoy writing terse but readable code that performs its job well.</p>
	<p>I've been interested in design for as long as I can remember. I love evoking beautiful, intuitive user interfaces and implementing them using my programming skills. It's a great way for me to challenge myself, and I enjoy the journey of creating an experience as much as the result.</p>
	<p>My extracurricular interests could go on for pages, but highlights include music production, hiking, and scientific research including nanomaterials, molecular biology, and climate change.</p>
</main>

<style>
	main {
		padding-bottom: 2rem;
		display: flex;
		flex-flow: column;
		justify-content: center;
		align-items: center;
		gap: 1rem;
	}

	h2 {
		font-weight: bold;
		font-size: 1.5rem;
	}

	p:not(.banner) {
		max-width: min(35rem, 90vw);
	}

	p.banner {
		max-width: 90vw;
		color: white;
	}
</style>