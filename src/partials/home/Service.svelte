<script>
    import Icon from '@iconify/svelte';
    import Service from "../../content/service.json"
</script>

<section class="service">
    <div class="wrapper py-8">
        <div class="box grid g-8">
            <div class="grid sm g-4">
                <h2 class="text-c">Why Hostinger is Best?</h2>
                <p class="text-c">A wide variety of tools to satisfy advanced user and website developer needs.</p>
            </div>
            <div class="grid col-3 g-6">
                {#each Service as item}
                <div class="flex item-c bg-soft round-sm g-4 p-6">
                    <Icon icon={item.icon} width="24" />
                    <h3 class="text-c">{item.name}</h3>
                </div>
                {/each}
            </div>
        </div>
    </div>
</section>