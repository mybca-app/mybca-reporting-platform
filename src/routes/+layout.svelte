<script lang="ts">
	import './layout.css';
	import favicon from '$lib/assets/favicon.svg';
	import Header from '$lib/components/Header.svelte';

	let { children } = $props();
</script>

<svelte:head><link rel="icon" href={favicon} /></svelte:head>

<div class="max-w-[80ch] mx-auto px-5 py-3 text-text">
	<Header />
	<main>
		{@render children()}
	</main>
</div>
