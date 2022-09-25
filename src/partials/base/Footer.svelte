<script>
    import Icon from '@iconify/svelte';
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
                    <a class="flex item-c" href="/"><Icon icon="ant-design:facebook-filled" width="28" /></a>
                    <a class="flex item-c" href="/"><Icon icon="ant-design:twitter-outlined" width="28" /></a>
                    <a class="flex item-c" href="/"><Icon icon="ant-design:reddit-circle-filled" width="28" /></a>
                    <a class="flex item-c" href="/"><Icon icon="ant-design:instagram-outlined" width="28" /></a>
                    <a class="flex item-c" href="/"><Icon icon="ant-design:github-filled" width="28" /></a>
                </div>
            </div>
        </div>
        <div class="links flex flex-w g-4 py-6">
            <div class="item flex-1">
                <h3 class="py-2">Hosting</h3>
                <ul>
                    <li class="py-2"><a href="/">VPS Hosting</a></li>
                    <li class="py-2"><a href="/">Cloud Hosting</a></li>
                    <li class="py-2"><a href="/">WordPress Hosting</a></li>
                    <li class="py-2"><a href="/">Ecommerce Hosting</a></li>
                    <li class="py-2"><a href="/">Free Web Hosting</a></li>
                    <li class="py-2"><a href="/">Email Hosting</a></li>
                </ul>
            </div>
            <div class="item flex-1">
                <h3 class="py-2">Domain</h3>
                <ul>
                    <li class="py-2"><a href="/">Domain Transfer</a></li>
                    <li class="py-2"><a href="/">XYZ Domain</a></li>
                    <li class="py-2"><a href="/">Cheap Domains</a></li>
                    <li class="py-2"><a href="/">WHOIS Lookup</a></li>
                    <li class="py-2"><a href="/">Free SSL Certificate</a></li>
                    <li class="py-2"><a href="/">Free Domain Name</a></li>
                </ul>
            </div>
            <div class="item flex-1">
                <h3 class="py-2">Information</h3>
                <ul>
                    <li class="py-2"><a href="/">Migrate to Hostinger</a></li>
                    <li class="py-2"><a href="/">System Status</a></li>
                    <li class="py-2"><a href="/">Affiliate Program</a></li>
                    <li class="py-2"><a href="/">Payment Methods</a></li>
                    <li class="py-2"><a href="/">Rewards</a></li>
                </ul>
            </div>
            <div class="item flex-1">
                <h3 class="py-2">Company</h3>
                <ul>
                    <li class="py-2"><a href="/">About Hostinger</a></li>
                    <li class="py-2"><a href="/">Our Technology</a></li>
                    <li class="py-2"><a href="/">Customer Care</a></li>
                    <li class="py-2"><a href="/">Roadmap</a></li>
                    <li class="py-2"><a href="/">Blog</a></li>
                </ul>
            </div>
            <div class="item flex-1">
                <h3 class="py-2">Legal & Help</h3>
                <ul>
                    <li class="py-2"><a href="/">About us</a></li>
                    <li class="py-2"><a href="/">Contact us</a></li>
                    <li class="py-2"><a href="/">Privacy Policy</a></li>
                    <li class="py-2"><a href="/">Terms of Service</a></li>
                    <li class="py-2"><a href="/">Report Online Abuse</a></li>
                </ul>
            </div>
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