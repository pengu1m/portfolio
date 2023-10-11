<script lang="ts">
    export let vec: number;
    export let hor: number;

    if (vec < 1) {
        throw new Error("'vec' of <Grid/> should be over 1!");
    }

    if (hor < 1) {
        throw new Error("'hor' of <Grid/> should be over 1!");
    }
</script>

<div class="my-5" style="--row:{vec}; --column: {hor};">
    <slot />
</div>

<style>
    div {
        display: grid;

        grid-template-rows: repeat(var(--row), 1fr);
        grid-template-columns: repeat(var(--column), 1fr);

        gap: 1rem;
    }

    @media screen and (max-width: 768px) {
        div {
            grid-template-columns: 1fr;
        }
    }
</style>
