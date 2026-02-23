<script lang="ts">
	import { onMount } from 'svelte';
	import favicon from '$lib/assets/favicon.svg';
	import 'bootstrap/dist/css/bootstrap.min.css';

	let { children } = $props();

	$effect(() => {
        // @ts-ignore - Ignora a linha abaixo na verificação
        import('bootstrap/dist/js/bootstrap.bundle.min.js');
    });
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
</svelte:head>

{@render children()}
