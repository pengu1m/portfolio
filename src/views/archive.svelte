<script lang="ts">
    import contacts from "../content/contacts.json";

    import Heading from "../components/heading.svelte";

    import Grid from "../components/grid.svelte";
    import Card from "../components/card.svelte";
    import List from "../components/list.svelte";
</script>

<div id="archive">
    <Heading text="🐙 Archive" />

    <Grid vec={1} hor={2}>
        <Card
            title="Github"
            img={{
                src: "https://github.githubassets.com/images/modules/logos_page/GitHub-Mark.png",
                alt: "Github logo",
            }}
        >
            <List
                flush={true}
                items={[
                    "프로젝트 & 개인 소스코드",
                    "수강 수업의 과제 코드",
                    "여러 잡동사니 & 문서 파일",
                ]}
            />

            <a
                class="btn btn-outline-primary d-block fw-bold mt-3"
                href={contacts.github.link}
            >
                🐙 {contacts.github.name}
            </a>
        </Card>

        <Card
            title="Blog"
            img={{
                src: "https://cdn-icons-png.flaticon.com/512/4922/4922073.png",
                alt: "blog image",
            }}
        >
            <List
                flush={true}
                items={["공부 & 지식 공유", "프로그래밍 스킬", "개인적인 생각"]}
            />

            <a
                class="btn btn-outline-primary d-block fw-bold mt-3"
                href={contacts.blog.link}
            >
                ✒️ {contacts.blog.name}
            </a>
        </Card>
    </Grid>
</div>
