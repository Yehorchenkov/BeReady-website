<script lang="ts">
	import '../app.css';

	import Header from '$lib/header.svelte'

	let { children } = $props();
</script>

<Header />

<div class="pt-16">
	{@render children()}
</div>
