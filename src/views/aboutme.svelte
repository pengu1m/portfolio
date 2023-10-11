<script lang="ts">
    import contacts from "../content/contacts.json";

    import Heading from "../components/heading.svelte";
    import Alert from "../components/alert.svelte";

    import Grid from "../components/grid.svelte";
</script>

<div id="about">
    <Heading text="🖐️ About me" />

    <Grid vec={2} hor={3}>
        <span class="text-center fw-bold h4"> 빨간 모자 펭귄 </span>
        <span class="text-center fw-bold h4"> 07년 생 </span>
        <span class="text-center fw-bold h4">
            <a href="https://maps.app.goo.gl/ELsLbyk6ZZoXVVfp8">남극</a> 출신
        </span>
        <span class="text-center fw-bold h4"> 취미: 코딩, 글쓰기 </span>
        <span class="text-center fw-bold h4">
            <a href={contacts.email.link}>이메일</a>
        </span>
        <span class="text-center fw-bold h4">
            <a href={contacts.discord.link}>디스코드</a>
        </span>
    </Grid>

    <Alert text="과외 & 외주 문의는 위의 연락처로!" />
</div>
