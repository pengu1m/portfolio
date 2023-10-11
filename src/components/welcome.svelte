<script lang="ts">
    export let title: string;
    export let description: string;
    export let btn: {
        href: string;
        text: string;
    };
</script>

<div class="p-5 mb-4 bg-body-tertiary rounded-3">
    <div class="container-fluid p-jumbo">
        <h1 class="display-5 fw-bold">{title}</h1>
        <p class="col-md-8 fs-4 mb-5">
            {description}
        </p>
        <a class="btn btn-primary btn-lg" href={btn.href}>{btn.text}</a>
    </div>
</div>

<style>
    .p-jumbo {
        padding-top: 30vh;
        padding-bottom: 50vh;
    }

    p {
        word-break: keep-all;
    }
</style>
