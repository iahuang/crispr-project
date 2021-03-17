<script lang="ts">
    export let split: number = 50;
    export let between: number = 5;

    function gridTemplateCols() {
        let a = split - between / 2;
        let b = 100 - split + between / 2;
        return `grid-template-columns: ${a}% ${between}% ${b}%;`;
    }
</script>

<div class="two-col" style={gridTemplateCols()}>
    <div class="first"><slot name="first" /></div>
    <div class="second"><slot name="second" /></div>
</div>

<style>
    .two-col {
        width: 100%;
        display: grid;
    }

    .first {
        grid-column: 1;
    }

    .second {
        grid-column: 3;
    }
</style>
