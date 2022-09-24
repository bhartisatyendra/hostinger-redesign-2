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
                    <li class="py-2">VPS Hosting</li>
                    <li class="py-2">Cloud Hosting</li>
                    <li class="py-2">WordPress Hosting</li>
                    <li class="py-2">Ecommerce Hosting</li>
                    <li class="py-2">Free Web Hosting</li>
                    <li class="py-2">Email Hosting</li>
                </ul>
            </div>
            <div class="item flex-1">
                <h3 class="py-2">Domain</h3>
                <ul>
                    <li class="py-2">Domain Transfer</li>
                    <li class="py-2">XYZ Domain</li>
                    <li class="py-2">Cheap Domains</li>
                    <li class="py-2">WHOIS Lookup</li>
                    <li class="py-2">Free SSL Certificate</li>
                    <li class="py-2">Free Domain Name</li>
                </ul>
            </div>
            <div class="item flex-1">
                <h3 class="py-2">Information</h3>
                <ul>
                    <li class="py-2">Migrate to Hostinger</li>
                    <li class="py-2">System Status</li>
                    <li class="py-2">Affiliate Program</li>
                    <li class="py-2">Payment Methods</li>
                    <li class="py-2">Rewards</li>
                </ul>
            </div>
            <div class="item flex-1">
                <h3 class="py-2">Company</h3>
                <ul>
                    <li class="py-2">About Hostinger</li>
                    <li class="py-2">Our Technology</li>
                    <li class="py-2">Customer Care</li>
                    <li class="py-2">Roadmap</li>
                    <li class="py-2">Blog</li>
                </ul>
            </div>
            <div class="item flex-1">
                <h3 class="py-2">Legal & Help</h3>
                <ul>
                    <li class="py-2">About us</li>
                    <li class="py-2">Contact us</li>
                    <li class="py-2">Privacy Policy</li>
                    <li class="py-2">Terms of Service</li>
                    <li class="py-2">Report Online Abuse</li>
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