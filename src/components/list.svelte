<script lang="ts">
    export let title: string | undefined = undefined;
    export let items: Array<string>;
    export let flush: boolean | undefined = undefined;

    let flush_classname: string = "";

    if (flush === undefined) {
        flush = false;
    }

    if (flush) {
        flush_classname = "list-group-flush";
    } else {
        flush_classname = "";
    }
</script>

<ul class="list-group {flush_classname} my-3">
    {#if title !== undefined}
        <li class="list-group-item list-group-item-primary fw-bold">{title}</li>
    {/if}

    {#each items as item}
        <li class="list-group-item">{item}</li>
    {/each}
</ul>
