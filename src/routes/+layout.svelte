<script lang="ts">
	import './layout.css';
	import favicon from '$lib/assets/favicon.svg';
	import { bg, bg2 } from '$lib/uitils/classUtils';
	import Header from '$lib/components/header.svelte';
	import Footer from '$lib/components/footer.svelte';

	let { children } = $props();
</script>

<svelte:head><link rel="icon" href={favicon} /></svelte:head>

<div class="flex flex-col h-screen w-screen {bg} justify-center items-center">
<Header></Header>
<main class="h-full lg:w-[80%] w-full px-2 flex flex-col overflow-y-auto scrollbar-hover">
	{@render children()}
</main>
<Footer></Footer>
</div>
