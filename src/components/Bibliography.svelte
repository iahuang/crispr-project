<script lang="ts">
    import type { MLASource } from "../mla";
    import BibliCitation from "./BibliCitation.svelte";

    export let websiteSources: MLASource[];
</script>

<div class="bib">
    <h1>Bibliography</h1>
    <ul>
        {#each websiteSources as source}
            <li><BibliCitation {source} /></li>
        {/each}
    </ul>
</div>

<style>
    li {
        font-size: 10pt;  
    }
</style>
