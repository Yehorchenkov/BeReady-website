<script lang="ts">
    import Hero from './main-page/hero.svelte';
	import StakeholderBlocks from './main-page/StakeholderBlocks.svelte';
    import ThematicBlocks from './main-page/ThematicBlocks.svelte';
</script>

<div class="max-w-screen-xl mx-auto">
    <Hero />
</div>

<div class="mt-16 max-w-screen-xl mx-auto">
    <h1 class="text-center font-bold text-2xl mb-4">Thematic Blocks</h1>
    <ThematicBlocks />
</div>

<div class="mt-16 max-w-screen-xl mx-auto">
    <h1 class="text-center font-bold text-2xl">Stakeholder Blocks</h1>
    <StakeholderBlocks />
</div>