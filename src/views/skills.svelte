<script lang="ts">
    import Heading from "../components/heading.svelte";
    import Grid from "../components/grid.svelte";

    import Card from "../components/card.svelte";
    import List from "../components/list.svelte";

    import { skills } from "../content/skills.json";
</script>

<div id="skills">
    <Heading text="⚔️ Skills" />

    <Grid hor={3} vec={2}>
        {#each skills as skill}
            <Card title={skill.title} img={skill.img}>
                {#each skill.list as sublist}
                    <List title={sublist.title} items={sublist.items} />
                {/each}
            </Card>
        {/each}
    </Grid>
</div>
