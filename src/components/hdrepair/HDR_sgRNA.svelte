<script lang="ts">
    import HdrLabeled from "./HDR_Labeled.svelte";

    export let guidingStrand: string;
</script>

<HdrLabeled definition="The Cas9's sgRNA "
    ><div class="sg-rna">
        {guidingStrand}
    </div></HdrLabeled
>

<style>
    .sg-rna {
        font-size: 12pt;
        font-family: monospace;
        color: #5bffce;
        user-select: none;
        margin: 0;
    }
</style>