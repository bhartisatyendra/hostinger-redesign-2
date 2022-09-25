<script>
    import Icon from '@iconify/svelte';

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
                <div class="brdr round-md p-8">
                    <div class="grid g-2">
                        <h3 class="text-c">Shared Hosting</h3>
                        <p class="text-xs text-c">Ideal solution for beginners</p>
                    </div>
                    <div class="grid g-4 py-8">
                        <div class="save flex item-c just-c g-2">
                            <s>₹{isMonthly ? "329" : "3,948"}.00</s>
                            <span class="btn text-xs round-xl">SAVE 79%</span>
                        </div>
                        <div class="price flex just-c lh-sm g-1">
                            <div class="text-lg">₹</div>
                            <p>{isMonthly ? "69" : "828"}.00</p>
                            <span class="text-lg">/mo</span>
                        </div>
                    </div>
                    <ul class="feat grid g-2">
                        <li><Icon icon="bi:check" width="24" color="#00ff00" /> 1 Website</li> 
                        <li><Icon icon="bi:check" width="24" color="#00ff00" /> 2 Databases</li> 
                        <li><Icon icon="bi:check" width="24" color="#00ff00" /> 1 Email Account</li> 
                        <li><Icon icon="bi:check" width="24" color="#00ff00" /> 50 GB SSD Storage</li> 
                        <li><Icon icon="bi:check" width="24" color="#00ff00" /> 100 GB Bandwidth</li>
                        <li><Icon icon="bi:check" width="24" color="#00ff00" /> Managed WordPress</li> 
                        <li><Icon icon="bi:check" width="24" color="#00ff00" /> ~10 000 Visits Monthly</li> 
                        <li><Icon icon="eva:close-fill" width="24" color="#ff0000" /> Free Domain - ₹749.00</li> 
                        <li><Icon icon="bi:check" width="24" color="#00ff00" /> 99.9% Uptime Guarantee</li> 
                        <li><Icon icon="bi:check" width="24" color="#00ff00" /> 24/7 Support</li>
                    </ul>
                    <div class="flex just-c">
                        <a class="btn round-sm" href="/">Add to cart</a>
                    </div>
                </div>
                <div class="bg-soft round-md p-8">
                    <div class="grid g-2">
                        <h3 class="text-c">WordPress Hosting</h3>
                        <p class="text-xs text-c">Perfect package for personal websites</p>
                    </div>
                    <div class="grid g-4 py-8">
                        <div class="save flex item-c just-c g-2">
                            <s>₹{isMonthly ? "649" : "7,788"}.00</s>
                            <span class="btn text-xs round-xl">SAVE 62%</span>
                        </div>
                        <div class="price flex just-c lh-sm g-1">
                            <div class="text-lg">₹</div>
                            <p>{isMonthly ? "249" : "2,988"}.00</p>
                            <span class="text-lg">/mo</span>
                        </div>
                    </div>
                    <ul class="feat grid g-2">
                        <li><Icon icon="bi:check" width="24" color="#00ff00" /> 100 Websites</li>
                        <li><Icon icon="bi:check" width="24" color="#00ff00" /> 200 GB SSD Storage</li>
                        <li><Icon icon="bi:check" width="24" color="#00ff00" /> ~1,00,000 Visits Monthly</li>
                        <li><Icon icon="bi:check" width="24" color="#00ff00" /> 250 GB SSD Storage</li>
                        <li><Icon icon="bi:check" width="24" color="#00ff00" /> Free Domain - ₹749.00</li>
                        <li><Icon icon="bi:check" width="24" color="#00ff00" /> Unlimited Bandwidth</li>
                        <li><Icon icon="bi:check" width="24" color="#00ff00" /> Unlimited Free SSL</li>
                        <li><Icon icon="bi:check" width="24" color="#00ff00" /> Managed WordPress</li>
                        <li><Icon icon="bi:check" width="24" color="#00ff00" /> 99.9% Uptime Guarantee</li>
                        <li><Icon icon="bi:check" width="24" color="#00ff00" /> 24/7 Support</li>
                    </ul>
                    <div class="flex just-c">
                        <a class="btn round-sm" href="/">Add to cart</a>
                    </div>
                </div>
                <div class="brdr round-md p-8">
                    <div class="grid g-2">
                        <h3 class="text-c">Cloud Hosting</h3>
                        <p class="text-xs text-c">Best Hosting for Professionals</p>
                    </div>
                    <div class="grid g-4 py-8">
                        <div class="save flex item-c just-c g-2">
                            <s>₹{isMonthly ? "1,699" : "20,388"}.00</s>
                            <span class="btn text-xs round-xl">SAVE 53%</span>
                        </div>
                        <div class="price flex just-c lh-sm g-1">
                            <div class="text-lg">₹</div>
                            <p>{isMonthly ? "799" : "9,588"}.00</p>
                            <span class="text-lg">/mo</span>
                        </div>
                    </div>
                    <ul class="feat grid g-2">
                        <li><Icon icon="bi:check" width="24" color="#00ff00" /> 6 GB RAM</li>
                        <li><Icon icon="bi:check" width="24" color="#00ff00" /> 4 CPU Cores</li>
                        <li><Icon icon="bi:check" width="24" color="#00ff00" /> 300 Websites</li>
                        <li><Icon icon="bi:check" width="24" color="#00ff00" /> 250 GB SSD Storage</li>
                        <li><Icon icon="bi:check" width="24" color="#00ff00" /> Free Domain - ₹749.00</li>
                        <li><Icon icon="bi:check" width="24" color="#00ff00" /> Daily Backups - ₹1,380.00</li>
                        <li><Icon icon="bi:check" width="24" color="#00ff00" /> Unlimited Free SSL</li>
                        <li><Icon icon="bi:check" width="24" color="#00ff00" /> Dedicated IP Address</li>
                        <li><Icon icon="bi:check" width="24" color="#00ff00" /> 99.9% Uptime Guarantee</li>
                        <li><Icon icon="bi:check" width="24" color="#00ff00" /> 24/7 Support</li>
                    </ul>
                    <div class="flex just-c">
                        <a class="btn round-sm" href="/">Add to cart</a>
                    </div>
                </div>
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
    background-color: var(--main-color);
    z-index: 1;
    border-radius: 99px;
    left: 10px;
    transition: 0.2s ease;
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