<script>
    import Icon from '@iconify/svelte';
    import Pricing from "../../content/pricing.json";
    let isMonthly = true;
</script>

<section class="pricing">
    <div class="wrapper py-8">
        <div class="box grid g-8">
            <div class="grid sm g-4">
                <h2 class="text-c">Our Hosting Plan</h2>
                <p class="text-c">We prepared the best web hosting plan for you to start. You will be able to adjust plans as you go - our custom-built algorithm.</p>
                <div class="flex just-c py-2">
                    <div class="switch flex bg-soft round-xl p-2 {isMonthly ? 'active' : ''}">
                        <span class="flex-1" on:click={() => (isMonthly = true)}>Monthly</span>
                        <span class="flex-1" on:click={() => (isMonthly = false)}>Yearly</span>
                    </div>
                </div>
            </div>
            <div class="grid col-3 g-8">
                {#each Pricing as plan}
                <div class="brdr round-md p-8">
                    <div class="grid g-2">
                        <h3 class="text-c">{plan.title}</h3>
                        <p class="text-xs text-c">{plan.info}</p>
                    </div>
                    <div class="grid g-4 py-8">
                        <div class="save flex item-c just-c g-2">
                            <s>₹{isMonthly ? plan.price : (plan.price.replace(',' , '') * 12).toLocaleString('en-IN')}.00</s>
                            <span class="btn text-xs round-xl">
                                SAVE {Math.round((plan.price.replace(',' , '') - plan.offer.replace(',' , '')) / plan.price.replace(',' , '') * 100)}%
                            </span>
                        </div>
                        <div class="price flex just-c lh-sm g-1">
                            <div class="text-lg">₹</div>
                            <p>{isMonthly ? plan.offer : (plan.offer * 12).toLocaleString('en-IN')}.00</p>
                            <span class="text-lg">/mo</span>
                        </div>
                    </div>
                    <ul class="feat grid g-2">
                        {#each plan.features as features}
                        <li><Icon icon="bi:check" width="24" color="#00ff00" />{features}</li> 
                        {/each}
                    </ul>
                    <div class="flex just-c">
                        <a class="btn round-sm" href="/">Add to cart</a>
                    </div>
                </div>
                {/each}
            </div>
        </div>
    </div>
</section>

<style>
    .switch {
        position: relative;
    }
    .switch::before {
        content: "";
        position: absolute;
        display: flex;
        height: 42px;
        width: 92px;
        left: 10px;
        background-color: var(--main-color);
        border-radius: 2.5rem;
        transition: 0.2s ease;
        z-index: 1;
    }
    .switch:not(.active):before {
        left: 50%;
    }
    .switch span {
        display: flex;
        align-items: center;
        justify-content: center;
        cursor: pointer;
        padding: 8px 20px;
        color: var(--bold-color);
        user-select: none;
        width: 92px;
        z-index: 2;
    }
    .save .btn {
        cursor: text;
        padding: 2px 8px;
    }
    .price {
        color: var(--bold-color);
    }
    .price p {
        font-size: 2.5rem;
    }
    .price span {
        align-self: end;
        margin-bottom: .25rem;
    }
    .feat {
        padding-left: 1rem;
        margin-bottom: 2rem;
    }
    .feat li {
        display: flex;
        align-items: center;
        gap: .5rem;
    }
</style>