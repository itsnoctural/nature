<script lang="ts">
	import * as messages from '$lib/paraglide/messages.js';
</script>

<main
	class="bg-background border-border mx-auto mt-6 flex max-w-screen-xl flex-col gap-y-4 rounded-lg border p-3"
>
	<div class="flex flex-col gap-3 lg:flex-row">
		<img class="rounded-md" src="/reports/impact.webp" alt="Ukrainian War Impact" />
		<div class="flex flex-col">
			<span class="text-2xl">{messages.briefing_title()}</span>
			<p class="text-muted-foreground">{messages.briefing_description()}</p>
		</div>
	</div>

	<hr />

	<div class="flex flex-col gap-3 lg:flex-row">
		<img class="rounded-md" src="/reports/marine.webp" alt="Ukrainian War Impact" />
		<div class="flex flex-col">
			<span class="text-2xl">{messages.marine_title()}</span>
			<p class="text-muted-foreground">{messages.marine_description()}</p>
		</div>
	</div>
</main>
