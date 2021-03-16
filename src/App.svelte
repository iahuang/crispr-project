<script lang="ts">
	export let name: string;
	import Bibliography from "./components/Bibliography.svelte";
import InlineImage from "./components/InlineImage.svelte";
import type { MLASource } from "./mla";

	const sources: MLASource[] = [
		{
			author: "Suzan Howler",
			title: "Top 10 Anime Deaths",
			organization: "Harvard University",
			url: "https://urmom.com"
		}
	]
</script>
<main>
	<h1>Hello {name}!</h1>
	<p>Visid the <a href="https://svelte.dev/tutorial">Svelte tutorial</a> to learn how to build Svelte apps.</p>
	<InlineImage url="https://fedoramagazine.org/wp-content/uploads/2015/03/test-days-945x400.png" width={100}></InlineImage>
	<Bibliography websiteSources={sources}></Bibliography>
	
</main>

<style>
	
</style>