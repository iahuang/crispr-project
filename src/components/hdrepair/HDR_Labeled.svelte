<script lang="ts">
    export let definition: string = "No definition provided.";
    let pos = { left: 0, top: 0 };
    let el: HTMLElement | null;
    let hovering = false;

    function onMouseEnter(ev: MouseEvent) {
        if (el) {
            let rect = el.getBoundingClientRect();
            pos.left = ev.pageX;
            pos.top = ev.pageY - window.scrollY;
        }
        hovering = true;
    }

    function onMouseLeave() {
        hovering = false;
    }
</script>

<span
    bind:this={el}
    class="term"
    on:mouseover={onMouseEnter}
    on:mouseleave={onMouseLeave}
    on:blur={onMouseLeave}
    on:mousemove={onMouseEnter}><slot /></span
>

{#if hovering}
    <div class="defbox" style={`left: ${pos.left}px; top: ${pos.top}px;`}>
        {definition}
    </div>
{/if}

<style>
    .term {
        cursor: pointer;
    }

    .defbox {
        position: fixed;
        padding: 20px;
        border-radius: 5px;
        box-shadow: 0px 5px 10px rgba(0, 0, 0, 0.356);
        background-color: white;
        pointer-events: none;
        max-width: 20vw;
        font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen, Ubuntu, Cantarell, "Open Sans",
            "Helvetica Neue", sans-serif;
        font-size: medium;
        z-index: 100;
        color: black;
    }
</style>
