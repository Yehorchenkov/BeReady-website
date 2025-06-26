<script lang="ts">
	import * as Card from '$lib/components/ui/card/index.js';
	import cardData from '$lib/data/thematic-blocks.json';
	import { Button } from '$lib/components/ui/button/index.js';

	interface CardItem {
		id: number;
		title: string;
		content: string;
		ref: string;
	}

	const cards: CardItem[] = cardData;
</script>

<section class="py-8 px-4">	<div class="grid grid-cols-1 md:grid-cols-3 lg:grid-cols-5 gap-6">
		{#each cards as card (card.id)}
			<Card.Root class="flex flex-col h-full pb-4">
				<Card.Header>
					<Card.Title>{card.title}</Card.Title>
				</Card.Header>
				<Card.Content class="flex-grow">
					<p>{card.content}</p>
				</Card.Content>
				<Card.Footer class="flex justify-center mt-auto">
					<Button variant="outline" href="{card.ref}">
						Continue reading
					</Button>
				</Card.Footer>
			</Card.Root>
		{/each}
	</div>
</section>
