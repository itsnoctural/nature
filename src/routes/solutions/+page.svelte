<script lang="ts">
	import * as messages from '$lib/paraglide/messages.js';

	interface ISite {
		name: string;
		description: string;
		href: string;
	}

	let sites: ISite[] = [
		{
			name: 'People in Need',
			description: messages.indeed(),
			href: 'https://climate.peopleinneed.net'
		},
		{
			name: 'Natural Resources Defense Council',
			description: messages.nrdc(),
			href: 'https://www.nrdc.org'
		}
	];
</script>

<main class="mx-auto mt-4 flex max-w-screen-xl flex-col gap-y-6">
	<div
		class="border-border bg-background/80 flex w-full flex-col gap-y-4 rounded-lg border px-6 py-4"
	>
		{#each sites as site}
			<a class="flex w-full flex-col gap-x-3" href={site.href}>
				<span>{site.name}</span>
				<span class="text-muted-foreground max-w-2/3 text-sm">{site.description}</span>
			</a>
		{/each}
	</div>
</main>
