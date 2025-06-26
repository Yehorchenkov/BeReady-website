<script lang="ts">
	import * as Card from '$lib/components/ui/card/index.js';
	import rawData from '$lib/data/stakeholder-blocks.json';
	import { Button } from '$lib/components/ui/button/index.js';

	const imgs = import.meta.glob('$lib/images/stakeholder-card/*.{png,jpg,jpeg,svg,gif}', {
		eager: true, // load immediately
		query: '?enhanced', // use ?enhanced for optimized images
		import: 'default'
	}) as Record<string, any>;

	const cards = rawData.map((d) => ({
		...d,
		// d.src in the JSON should be just 'photo.jpg' or 'folder/photo.jpg'
		src: imgs[`/src/lib/images/stakeholder-card/${d.src}`] // Use the actual resolved path
	}));

</script>

<section class="px-4 py-8">
	<div class="grid grid-cols-1 gap-6 md:grid-cols-3 lg:grid-cols-5">
		{#each cards as card (card.id)}
			<Card.Root class="flex h-full flex-col overflow-hidden pt-0 pb-4">
				<div class="h-48 w-full">
					<enhanced:img src={card.src} alt={card.alt} class="h-full w-full object-cover" />
				</div>

				<Card.Header>
					<Card.Title>{card.title}</Card.Title>
				</Card.Header>

				<Card.Footer class="mt-auto flex justify-center">
					<Button variant="outline" href={card.ref}>Continue reading</Button>
				</Card.Footer>
			</Card.Root>
		{/each}
	</div>
</section>