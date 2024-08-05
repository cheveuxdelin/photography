<script lang="ts">
	import { capitalize } from "$lib/functions.js";
	export let data;
	let title: string;
	$: {
		title = capitalize(data.location);
	}
</script>

<div class="w-fit mx-auto px-2 my-24">
	<h1 class="text-4xl mb-24 text-center font-thin">{title}</h1>

	<!-- svelte-ignore a11y-missing-attribute -->
	<div class=" grid gap-2 sm:grid-cols-3">
		{#each { length: 27 } as _}
			<img src="/wasabi.jpg" class="w-fit aspect-square sm:w-[400px] object-cover" />
		{/each}
	</div>
</div>

