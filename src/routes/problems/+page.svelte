<script lang="ts">
	import * as messages from '$lib/paraglide/messages.js';
</script>

<main
	class="bg-background border-border mx-auto mt-6 flex max-w-screen-xl flex-col gap-y-4 rounded-lg border p-3"
>
	<a
		class="flex flex-col gap-3 lg:flex-row"
		href="https://ceobs.org/ukraine-conflict-environmental-briefing-the-climate-crisis/"
	>
		<img class="rounded-md" src="/reports/impact.webp" alt="Ukrainian War Impact" />
		<div class="flex flex-col">
			<span class="text-2xl">{messages.briefing_title()}</span>
			<p class="text-muted-foreground">{messages.briefing_description()}</p>
		</div>
	</a>

	<hr />

	<a class="flex flex-col gap-3 lg:flex-row" href="https://doi.org/10.1186/s12995-023-00398-y">
		<img class="rounded-md" src="/reports/marine.webp" alt="Ukrainian War Impact" />
		<div class="flex flex-col">
			<span class="text-2xl">{messages.marine_title()}</span>
			<p class="text-muted-foreground">{messages.marine_description()}</p>
		</div>
	</a>
</main>
