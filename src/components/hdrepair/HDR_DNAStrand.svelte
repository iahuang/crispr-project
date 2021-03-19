<script lang="ts">
    import HdrLabeled from "./HDR_Labeled.svelte";

    export let bases: string = "AAA";
    export let definition: string = "";

    function complementaryBase(base: string) {
        return {
            A: "T",
            G: "C",
            T: "A",
            C: "G",
        }[base] || " ";
    }
</script>

<span class="dna-strand-a">
    <HdrLabeled {definition}>{bases}</HdrLabeled>
</span>
<span class="dna-strand-b">
    <HdrLabeled {definition}
        >{Array.from(bases)
            .map((c) => complementaryBase(c))
            .join("")}</HdrLabeled
    >
</span>

<style>
    .dna-strand-a {
        font-size: 12pt;
        font-family: monospace;
        color: #ff8e2b;
        user-select: none;
        margin:0;
    }

    .dna-strand-b {
        font-size: 12pt;
        font-family: monospace;
        color: #5ba7ff;
        user-select: none;
        margin:0;
    }
</style>
