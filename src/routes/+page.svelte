<script lang="ts">
	import * as messages from '$lib/paraglide/messages.js';
</script>

<main class="mx-auto mt-6 flex max-w-screen-lg flex-col justify-between gap-4 lg:flex-row">
	<img class="border-border rounded-2xl border-3" src="/planet.webp" alt="Planet" />

	<div class="flex w-full max-w-full flex-col gap-y-2 text-right lg:max-w-1/2">
		<h1 class="text-4xl font-semibold">{messages.why()}</h1>
		<p class="text-muted-foreground">{messages.why_answer()}</p>
	</div>
</main>
