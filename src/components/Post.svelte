<script>
    import readingTime from "../utils/readingTime";
    import randomEmoji from "../utils/randomEmoji";
    import formatIsoTime from "../utils/formatIsoTime";
    export let post;
</script>

<style>
    .Post-item {
        color: #191a22;
        position: relative;
    }
    .Post-content {
        font-size: 16px;
        font-weight: 300;
        display: grid;
        grid-template-columns: 1fr;
        grid-gap: 5px;
        justify-content: space-between;
    }
    .Post-title p {
        color: #333;
        font-size: 13px;
        font-weight: 300;
        margin-top: 5px;
        padding: 0;
    }
    a {
        text-decoration: none;
        color: #22215b;
    }
    .Post-desc {
        color: #333;
        font-size: 16px;
        line-height: 28px;
        margin: 0 auto;
        word-break: break-word;
    }
    .dot {
        font-weight: 700;
    }
</style>

<div class="Post-item">
    <div class="Post-content">
        <div class="Post-head">
            <div class="Post-title">
                <h2>
                    <a
                        rel="prefetch"
                        href="blog/{post.slug}">{randomEmoji()}{post.title}</a>
                </h2>
                <p>
                    <time datatime={post.createdAt}>
                        {formatIsoTime(post.createdAt)}
                    </time>
                    <span class="dot">.</span>
                    <span>{readingTime(post.html)}</span>
                </p>
            </div>
            <div class="Post-tags" />
            <div class="Post-desc">
                <p>{post.description}</p>
            </div>
        </div>
    </div>
</div>
