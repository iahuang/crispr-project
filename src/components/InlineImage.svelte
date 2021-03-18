<script lang="ts">
    export let url: string;
    export let altText: string = "";
    export let scale: number = 100;
</script>

<div class="cont" style={`width:${scale}%;`}>
    <a href={url}><img src={url} alt={altText} /></a>
    <a href={url} class="link">{url}</a>
</div>

<style>
    .cont {
        display: inline-flex;
        flex-direction: column;
        align-items: center;
        overflow: hidden;
    }
    .link {
        word-wrap:break-word;
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
        width: 100%;
    }
</style>
