<script lang="ts">
    export let url: string;
    export let altText: string = "";
    export let scale: number = 100;
</script>

<div>
    <a href={url}><img src={url} alt={altText} style={`width:${scale}%;`}/></a>
    <a href={url}>{url}</a>
</div>

<style>
    div {
        display: inline-flex;
        flex-direction: column;
        align-items: center;
        max-width: 100%;
    }
    a {
        font-size: 7pt;
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
