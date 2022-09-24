<script>
    import Icon from '@iconify/svelte';
    import { onMount } from "svelte";
  
    let time = new Date();
  
    $: day = time.getDate() > 9 ? time.getDate() : "0" + time.getDate();
    $: hour = time.getHours() > 9 ? time.getHours() : "0" + time.getHours();
    $: min = time.getMinutes() > 9 ? time.getMinutes() : "0" + time.getMinutes();
    $: sec = time.getSeconds() > 9 ? time.getSeconds() : "0" + time.getSeconds();
  
    onMount(() => {
      const interval = setInterval(() => {
        time = new Date();
      }, 1000);
  
      return () => {
        clearInterval(interval);
      };
    });
</script>

<div class="herose">
    <div class="wrapper py-8">
        <div class="box sm flex flex-c just-c g-2 py-8">
            <h2 class="text-c">Savings to Set Your Website in Motion</h2>
            <p class="text-c lh-lg py-2">MWe prepared the best web hosting plan for you to start. You will be able to adjust plans as you go - our custom-built algorithm.</p>
            <div class="action flex just-c flex-c g-4 py-2">
                <a class="btn text-c round-xl" href="/">Get Started</a>
                <a class="btn outline text-c round-xl" href="/">View Plans</a>
            </div>
            <h3 class="text-c py-2">Get free .com domain for 1st year</h3>
            <div class="timer flex just-c flex-w g-4 py-2">
                <div class="flex item-c just-c flex-c flex-1 brdr round-sm p-2">
                    <p class="text-xl">{day}</p>
                    <span class="text-ss">Days</span>
                </div>
                <div class="flex item-c just-c flex-c flex-1 brdr round-sm p-2">
                    <p class="text-xl">{hour}</p>
                    <span class="text-ss">Hours</span>
                </div>
                <div class="flex item-c just-c flex-c flex-1 brdr round-sm p-2">
                    <p class="text-xl">{min}</p>
                    <span class="text-ss">Minutes</span>
                </div>
                <div class="flex item-c just-c flex-c flex-1 brdr round-sm p-2">
                    <p class="text-xl">{sec}</p>
                    <span class="text-ss">Seconds</span>
                </div>
            </div>
            <p class="flex item-c just-c g-1 text-xs"><Icon icon="bi:check" width="24" color="#00ff00" /> Get exclusive 30-day money-back guarantee*</p>
        </div>
    </div>
</div>

<style>
    .herose {
        padding: 1.5rem 0;
        background: url("/liquid-cheese.svg");
        background-repeat: no-repeat;
        background-size: cover;
    }
    .box {
        padding: 1rem;
    }
    .box h2 {
        font-size: 1.75rem;
    }
    .action .btn {
        padding: 12px 32px;
    }
    .timer > * {
        min-width: 80px;
        min-height: 80px;
    }
    @media (min-width: 576px) {
        .timer > * {
            flex: 0;
        }
        .action {
            flex-direction: row;
        }
    }
    @media (min-width: 768px) {
        .box h2 {
            font-size: 3rem;
        }
    }
</style>