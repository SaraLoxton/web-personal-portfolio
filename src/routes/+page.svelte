<script>
  import Hero from '$lib/components/home/Hero.svelte';
  import AboutPreview from '$lib/components/home/AboutPreview.svelte';
  import FeaturedProjects from '$lib/components/home/FeaturedProjects.svelte';
  import Skills from '$lib/components/home/Skills.svelte';
  import ContactCTA from '$lib/components/home/ContactCTA.svelte';
</script>

<svelte:head>
  <title>Sara Loxton | Spatial Data Science Portfolio</title>
  <meta
    name="description"
    content="Portfolio of Sara Loxton - Spatial Data Science student building geospatial, data-driven, and community-focused digital projects."
  />
</svelte:head>

<div class="home-page">
  <Hero />
  <AboutPreview />
  <Skills />
  <FeaturedProjects />
  <ContactCTA />
</div>

<style lang="scss">
  .home-page {
    width: 100%;
    overflow-x: clip;
  }
</style>