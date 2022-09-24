<script>
  import Herose from "../partials/home/Herose.svelte";
  import Service from "../partials/home/Service.svelte";
  import Pricing from "../partials/home/Pricing.svelte";
  import Update from "../partials/home/Update.svelte";
  import Review from "../partials/home/Review.svelte";
</script>

<svelte:head>
	<title>Hostinger Redesign</title>
  <meta name="description" content="Hostinger Redesign by Sherman. Powered By SvelteKit.">
</svelte:head>

<main class="content">

    <Herose />

    <Service />
    
    <Pricing />

    <Review />

    <Update />
    
</main>