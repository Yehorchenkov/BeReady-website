<script lang="ts">
	import * as NavigationMenu from '$lib/components/ui/navigation-menu/index.js';
	import { navigationMenuTriggerStyle } from '$lib/components/ui/navigation-menu/navigation-menu-trigger.svelte';
	import thematicBlocks from '$lib/data/thematic-blocks.json';
    import stakeholderBlocks from '$lib/data/stakeholder-blocks.json';
</script>

<NavigationMenu.Root viewport={false}>
	<NavigationMenu.List>
		<NavigationMenu.Item>
			<NavigationMenu.Trigger>Thematic Blocks</NavigationMenu.Trigger>
			<NavigationMenu.Content>
				<ul class="grid w-[400px] gap-2 p-4">
					{#each thematicBlocks as block}
						<li>
							<NavigationMenu.Link href={block.ref}>
								<div class="font-medium">{block.title}</div>
								<div class="text-muted-foreground text-sm">
									{block.content}
								</div>
							</NavigationMenu.Link>
						</li>
					{/each}
				</ul>
			</NavigationMenu.Content>
		</NavigationMenu.Item>
		<NavigationMenu.Item>
			<NavigationMenu.Trigger>Stakeholder Blocks</NavigationMenu.Trigger>
			<NavigationMenu.Content>
				<ul class="grid w-[200px] gap-4 p-2">
                    {#each stakeholderBlocks as block}
                        <li>
                            <NavigationMenu.Link href={block.ref}>
                                {block.title}
                            </NavigationMenu.Link>
                        </li>
                    {/each}
				</ul>
			</NavigationMenu.Content>
		</NavigationMenu.Item>
		<NavigationMenu.Item>
			<NavigationMenu.Link>
				{#snippet child()}
					<a href="/" class={navigationMenuTriggerStyle()}>Repository</a>
				{/snippet}
			</NavigationMenu.Link>
		</NavigationMenu.Item>
	</NavigationMenu.List>
</NavigationMenu.Root>
