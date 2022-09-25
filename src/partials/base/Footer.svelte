<script>
    import Icon from '@iconify/svelte';
    import Footer from "../../content/footer.json";
    import Social from "../../content/social.json";
</script>

<footer class="footer">
    <div class="wrapper py-2">
        <div class="about brdr-b py-8">
            <div class="brand flex flex-c just-b g-4 py-4">
                <div class="logo flex item-c">
                    <a href="/">Hostinger</a> 
                </div>
                <p class="flex-1">Lorem ipsum dolor sit amet consectetur adipisicing elit. Non minus corrupti est mollitia modi sunt reprehenderit, cumque, provident beatae, voluptatem quod autem quia eos?</p>
                <div class="social flex g-6 py-2">
                    {#each Social as item}
                    <a class="flex item-c" href={item.link} target="_blank" title={item.name}>
                        <Icon icon={item.icon} width="28" />
                    </a>
                    {/each}
                </div>
            </div>
        </div>
        <div class="links flex flex-w g-4 py-6">
            {#each Footer as item}
            <div class="item flex-1">
                <h3 class="py-2">{item.name}</h3>
                <ul>
                    {#each item.child as child}
                    <li class="py-2"><a href={child.link}>{child.name}</a></li>
                    {/each}
                </ul>
            </div>
            {/each}
        </div>
        <div class="tmark flex flex-c just-b g-2 brdr-t py-8">  
           <p class="flex just-c">&copy; 2022 Hostinger All rights reserved</p>                                                                                            
           <p class="flex item-c just-c g-2">Redesign with <Icon icon="ant-design:heart-filled" width="16" color="red" /> By Sherman</p>
        </div>
    </div>
</footer>

<style>
    .footer {
        border-top: 1px solid var(--brdr-color);
    }
    .links .item {
        min-width: 160px;
    }
    @media (min-width: 768px) {
        .tmark {
            flex-direction: row;
        }
    }
    @media (min-width: 992px) {
        .brand {
            flex-direction: row;
        }
        .logo, 
        .social {
            margin: 0 2.5rem;
        }
    }
</style>