<div>
    <slot />
</div>

<style>
    div {
        width: 80vw;
        margin: auto;
    }

    @media screen and (max-width: 768px) {
        div {
            width: 95vw;
        }
    }
</style>
