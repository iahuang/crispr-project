<script lang="ts">
    import type { MLASource } from "../mla";

    export let source: MLASource;
</script>

{source.author || "Unknown Author"}. <i>{source.title}</i>. {source.organization || "N/A"}, {source.date || "Unknown Date"},
<a href={source.url}>{source.url}</a>. Accessed 16 March 2021.
