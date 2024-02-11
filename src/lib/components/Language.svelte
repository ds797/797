<script>
	import { cubicOut } from 'svelte/easing';
	import Proficiency from '$lib/components/Proficiency.svelte';
	import expand from '$lib/assets/expand.svg';

	export let language;

	let children = false;

	const slide = (node, { delay = 0, duration = 400, easing = cubicOut } = {}) => {
    const style = getComputedStyle(node);
    const opacity = +style.opacity;
    const height = parseFloat(style.height);
    const padding_top = parseFloat(style.paddingTop);
    const padding_bottom = parseFloat(style.paddingBottom);
    const margin_top = parseFloat(style.marginTop);
    const margin_bottom = parseFloat(style.marginBottom);
    const margin_left = parseFloat(style.marginLeft);
    const border_top_width = parseFloat(style.borderTopWidth);
    const border_bottom_width = parseFloat(style.borderBottomWidth);
    return {
        delay,
        duration,
        easing,
        css: t => 'overflow: hidden;' +
					`opacity: ${Math.min(t * 20, 1) * opacity};` +
					`height: ${t * height}px;` +
					`padding-top: ${t * padding_top}px;` +
					`padding-bottom: ${t * padding_bottom}px;` +
					`margin-top: ${t * margin_top}px;` +
					`margin-bottom: ${t * margin_bottom}px;` +
					`margin-left: ${t * margin_left}px;` +
					`border-top-width: ${t * border_top_width}px;` +
					`border-bottom-width: ${t * border_bottom_width}px;`
    };
	}
</script>

<main>
	<div class="main" style="{language.children && 'cursor: pointer;'}" on:click={() => children = !children}>
		<img src={expand} alt="Expand" style="{!language.children ? 'visibility: hidden;' : ''} {children ? 'transform: rotate(90deg);' : ''}" />
		<img src={language.icon} alt="Loading" />
		<div class="data">
			<h3>{language.name}</h3>
			<Proficiency proficiency={language.proficiency} />
		</div>
	</div>
	{ #if children && language.children }
		<div class="children" transition:slide>
			{ #each language.children as language }
				<svelte:self {language} />
			{ /each }
		</div>
	{ /if }
</main>

<style>
	main {
		display: flex;
		flex-flow: column;
		justify-content: center;
	}

	.main {
		width: 25rem;
		display: flex;
		align-items: center;
		gap: 1rem;
	}

	h1 {
		text-align: start;
	}

	.data {
		display: flex;
		flex-flow: column;
		justify-content: center;
		gap: 0.25rem;
	}

	.children {
		margin: 2rem 0 0 3rem;
		display: flex;
		flex-flow: column;
		gap: 2rem;
	}

	img {
		width: 3rem;
		height: 3rem;
		border-radius: 0.5rem;
	}
</style>