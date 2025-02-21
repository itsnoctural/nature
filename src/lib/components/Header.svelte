<script lang="ts">
	import { goto } from '$app/navigation';
	import { page } from '$app/state';
	import { i18n } from '$lib/i18n';
	import * as messages from '$lib/paraglide/messages.js';
	import { languageTag } from '$lib/paraglide/runtime.js';
	import ThemeToggle from './ThemeToggle.svelte';
	import Button from './ui/Button.svelte';

	function switchToLanguage() {
		const canonicalPath = i18n.route(page.url.pathname);
		const localisedPath = i18n.resolveRoute(canonicalPath, languageTag() == 'en' ? 'uk-ua' : 'en');
		goto(localisedPath);
	}
</script>

<header class="z-50 w-full">
	<div
		class="border-border bg-background/75 mx-auto flex h-14 w-full max-w-screen-xl items-center justify-between gap-x-1.5 rounded-xl border px-4"
	>
		<a class="text-base font-semibold sm:text-lg" href="/">savenature.ua</a>
		<nav class="flex gap-x-2 text-xs sm:text-base">
			<a class="underline underline-offset-4" href="/problems">{messages.problems()}</a>
			<a class="underline underline-offset-4" href="/solutions">{messages.solutions()}</a>
		</nav>
		<div class="flex items-center gap-x-1.5">
			<Button variant="outline" size="icon" onclick={switchToLanguage}>
				<img
					height="18"
					width="18"
					src={languageTag() == 'en' ? '/flags/usa.webp' : '/flags/ua.webp'}
					alt="Change language"
				/>
			</Button>
			<ThemeToggle />
		</div>
	</div>
</header>
