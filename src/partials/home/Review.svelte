<script>
    import Review from "../../content/review.json"
</script>

<section class="review">
    <div class="wrapper py-8">
        <div class="box grid g-8">
            <div class="grid sm g-4">
                <h2 class="text-c">Why People Love Hostinger</h2>
                <p class="text-c">People from 40+ countries trust their websites to Hostinger. Here's what our users say in their web hosting reviews from Trustpilot</p>
            </div>
            <div class="grid col-3 g-8">
                {#each Review as user}
                <div class="bg-soft round-sm p-8">
                    <div class="flex just-c">
                        <img  class="round-full" src={user.image} width="100" alt={user.name}>
                    </div>
                    <p class="text-c py-8">{user.content}</p>
                    <div class="grid g-1">
                        <h3 class="text-c">{user.name}</h3>
                        <div class="text-c">{user.jobTitle}</div>
                    </div>
                </div>
                {/each}
            </div>
        </div>
    </div>
</section>