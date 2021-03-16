<script lang="ts">
    export let url: string;
    export let altText: string = "";
    export let width: number;
</script>

<div>
    <a href={url}><img src={url} alt={altText} {width} /></a>
    <a href={url}>{url}</a>
</div>

<style>
    div {
        display: inline-flex;
        flex-direction: column;
        align-items: center;
    }
    a {
        font-size: 6pt;
        -webkit-user-drag: none;
        -khtml-user-drag: none;
        -moz-user-drag: none;
        -o-user-drag: none;
        user-drag: none;
    }
    img {
        -webkit-user-drag: none;
        -khtml-user-drag: none;
        -moz-user-drag: none;
        -o-user-drag: none;
        user-drag: none;
    }
</style>
