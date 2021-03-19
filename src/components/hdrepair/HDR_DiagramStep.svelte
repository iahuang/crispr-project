<script lang="ts">
    export let url: string;
</script>

<img class="step" src={url} alt={""} />

<style>
    .step {
        width: 50%;
        border-radius: 5px;
        box-shadow: 0px 5px 10px rgba(0, 0, 0, 0.356);
    }
</style>
