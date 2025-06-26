<script>
	import PageTemplate from '$lib/page-template.svelte';
	let { children } = $props();
</script>

<PageTemplate>
    {@render children()}
</PageTemplate>
