<script lang="ts">
    import Heading from "../components/heading.svelte";
    import Grid from "../components/grid.svelte";

    import Card from "../components/card.svelte";
    import Slide from "../components/slide.svelte";

    import { projects } from "../content/projects.json";
    import List from "../components/list.svelte";
    import Aboutme from "./aboutme.svelte";

    const project_count = projects.length;
</script>

<div id="projects">
    <Heading text="📦 Projects" />

    <Grid hor={1} vec={project_count}>
        {#each projects as project}
            <Card title={project.title}>
                <Grid hor={2} vec={1}>
                    <div>
                        <Slide imgs={project.thumbnails} />
                    </div>
                    <div class="fs-5">
                        <p class="text-center fw-bold">{project.description}</p>

                        <hr class="my-3" />

                        <ul>
                            <li>
                                <span class="fw-bold">Features:</span>
                                <ul>
                                    {#each project.features as feature}
                                        <li>{feature}</li>
                                    {/each}
                                </ul>
                            </li>
                            <li>
                                <span class="fw-bold">Tech Stack:</span>
                                <ul>
                                    {#each project.techstack as tech}
                                        <li>{tech}</li>
                                    {/each}
                                </ul>
                            </li>
                            <li>
                                <span class="fw-bold">Github:</span>
                                <a href={project.github}>
                                    Repository 바로가기
                                </a>
                            </li>
                            <li>
                                <span class="fw-bold">URL:</span>
                                <a href={project.deployment}> 배포 바로가기 </a>
                            </li>
                        </ul>
                    </div>
                </Grid>
            </Card>
        {/each}
    </Grid>
</div>
