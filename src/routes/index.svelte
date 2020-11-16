<script context="module">
    export function preload() {
        return this.fetch(`blog.json`)
            .then(r => r.json())
            .then(posts => {
                return { posts };
            });
    }
</script>

<script>
    import Post from "../components/Post.svelte";
    export let posts;
</script>

<style>
    .Posts {
        display: grid;
        grid-template-columns: 1fr;
        grid-gap: 15px;
        justify-content: space-between;
    }
</style>

<svelte:head>
    <title>Ismael López</title>
    <meta name="description" content="Blog de prueba de ismaellopezdev" />

    <meta name="twitter:card" content="summary_large_image" />
    <meta name="twitter:site" content="@ismaellopezdev" />
    <meta name="twitter:creator" content="@ismaellopezdev" />
    <meta name="twitter:title" content="Ismael López" />
    <meta
        name="twitter:description"
        content="Blog de prueba de ismaellopezdev" />
    <meta
        name="twitter:image"
        content="https://blog-on-svelte.netlify.app/blogpost-cover.png" />

    <meta name="og:title" content="Ismael López" />
    <meta name="og:description" content="Blog de prueba de ismaellopezdev" />
    <meta
        name="og:image"
        content="https://blog-on-svelte.netlify.app/blogpost-cover.png" />
    <meta name="og:url" content="https://blog-on-svelte.netlify.app" />
    <meta name="og:site_name" content="Ismael López" />
    <meta name="og:locale" content="es_ES" />
    <meta name="og:type" content="article" />
    <meta name="fb:app_id" content="" />
</svelte:head>

<div class="Home">
    <div class="Posts">
        {#each posts as post}
            <Post {post} />
        {/each}
    </div>
</div>
