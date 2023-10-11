<script lang="ts">
    import Img from "./img.svelte";

    // create random text (for id)
    const slide_id = "slide-" + Math.random().toString(36).substring(2, 11);
    const slide_selector = "#" + slide_id;

    export let imgs: Array<{
        src: string;
        alt: string;
    }>;
</script>

<div id={slide_id} class="carousel slide">
    <div class="carousel-inner">
        {#each imgs as img, index}
            {#if index === 1}
                <div class="carousel-item active">
                    <Img
                        src={img.src}
                        classname="d-block w-100 rounded"
                        alt={img.alt}
                    />
                </div>
            {:else}
                <div class="carousel-item">
                    <Img
                        src={img.src}
                        classname="d-block w-100 rounded"
                        alt={img.alt}
                    />
                </div>
            {/if}
        {/each}
    </div>
    <button
        class="carousel-control-prev"
        type="button"
        data-bs-target={slide_selector}
        data-bs-slide="prev"
    >
        <span class="carousel-control-prev-icon" aria-hidden="true" />
        <span class="visually-hidden">Previous</span>
    </button>
    <button
        class="carousel-control-next"
        type="button"
        data-bs-target={slide_selector}
        data-bs-slide="next"
    >
        <span class="carousel-control-next-icon" aria-hidden="true" />
        <span class="visually-hidden">Next</span>
    </button>
</div>

<style>
    .carousel.slide {
        border: gray 1px solid;
        border-radius: 7px;
    }
</style>
