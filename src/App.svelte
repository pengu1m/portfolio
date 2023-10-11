<script lang="ts">
    import Header from "./components/header.svelte";
    import Footer from "./components/footer.svelte";

    import Layout from "./components/layout.svelte";

    import WelcomeView from "./views/welcome.svelte";
    import AboutmeView from "./views/aboutme.svelte";
    import SkillsView from "./views/skills.svelte";
    import ArchiveView from "./views/archive.svelte";
    import ProjectsView from "./views/projects.svelte";
    import ContactsView from "./views/contacts.svelte";
</script>

<Header />

<WelcomeView />

<Layout>
    <hr />
    <AboutmeView />
    <hr />
    <SkillsView />
    <hr />
    <ArchiveView />
    <hr />
    <ProjectsView />
    <hr />
    <ContactsView />

    <Footer />
</Layout>
