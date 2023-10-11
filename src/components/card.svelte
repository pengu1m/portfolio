<script lang="ts">
    export let img: { src: string; alt: string } | undefined = undefined;
    export let title: string;

    import Img from "./img.svelte";
</script>

<div class="card p-3">
    {#if img !== undefined}
        <Img src={img.src} classname="card-img-top" alt={img.alt} />
    {/if}

    <hr />
    <div class="card-body">
        <h3 class="card-title fw-bold">{title}</h3>
        <slot />
    </div>
</div>
