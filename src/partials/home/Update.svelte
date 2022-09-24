<script>
    import Update from "../../content/update.json"
</script>

<section class="update">
    <div class="wrapper py-8">
        <div class="box grid g-8">
            <div class="grid sm g-4">
                <h2 class="text-c">Our Latest Updates</h2>
                <p class="text-c">Learn the latest Hostinger and hosting industry releases, trends and noteworthy news.</p>
            </div>
            <div class="grid col-3 g-8">
                {#each Update as post}
                <article class="flex flex-c g-4">
                    <a class="thumb" href="/">
                        <img src={post.image} alt={post.title}>
                    </a>
                    <div class="flex flex-c g-3">
                        <span>{post.date}</span>
                        <h3 class="text-lg">{post.title}</h3>
                        <p>{post.info}</p>
                        <span>By {post.author}</span>
                    </div>
                </article>
                {/each}
            </div>
        </div>
    </div>
</section>