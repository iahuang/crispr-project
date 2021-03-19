<script lang="ts">
    export let x: number = 0;
    export let y: number = 0;
</script>

<div style={`position: absolute; top: ${y}pt; left: ${x}pt;`}>
    <slot></slot>
</div>