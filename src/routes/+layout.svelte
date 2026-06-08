<script>
  import '../app.scss';
  import Nav from '$lib/components/layout/Nav.svelte';
  import Footer from '$lib/components/layout/Footer.svelte';
</script>

<Nav/>
<div class="site-shell">
  <main>
    <slot />
    
  </main>
</div>

<style lang="scss">
  .site-shell {
    min-height: 100vh;
    display: flex;
    flex-direction: column;
  }

  main {
    flex: 1;
  }
</style>