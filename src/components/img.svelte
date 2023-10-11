<script lang="ts">
    export let src: string;
    export let alt: string;
    export let classname: string | undefined = undefined;
</script>

<img {src} {alt} loading="lazy" class={classname} />
