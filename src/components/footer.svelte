<script lang="ts">
    import contacts from "../content/contacts.json";
</script>

<footer>
    <hr />

    <p>
        Deployed on Vercel <br />
        copyright &copy; Github,
        <a href={contacts.github.link}>{contacts.github.name}</a>
    </p>
</footer>

<style>
    p {
        text-align: center;
    }
</style>
