<script lang="ts">
	import './layout.css';
	import favicon from '$lib/assets/favicon.svg';
	import { bg } from '$lib/uitils/classUtils';

	let { children } = $props();
</script>

<svelte:head><link rel="icon" href={favicon} /></svelte:head>

<div class="flex flex-col h-screen w-screen {bg}">
	{@render children()}

</div>
