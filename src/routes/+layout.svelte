<script>
  import Nav from "../lib/Nav.svelte";
  import Footer from "../lib/Footer.svelte";
</script>

<Nav />
<main id="main">
  <slot />
</main>
<Footer />