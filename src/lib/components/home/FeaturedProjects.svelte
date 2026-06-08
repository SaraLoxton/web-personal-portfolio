<script>
  import SectionHeading from '$lib/components/ui/SectionHeading.svelte';
  import ProjectCard from '$lib/components/ui/ProjectCard.svelte';
  import { featuredProjects } from '$lib/data/projects';
</script>

<section class="featured section" id="featured-projects">
  <div class="container">
    <SectionHeading
      eyebrow="Featured Projects"
      title="Selected work that blends data, place, and digital design"
      description="A few projects that best represent the direction I’m building toward."
    />

    <div class="featured__grid">
      {#each featuredProjects as project}
        <ProjectCard {project} />
      {/each}
    </div>
  </div>
</section>

<style lang="scss">
  .featured {
    background: #0b1220;
  }

  .featured__grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 1.5rem;
    margin-top: 3rem;
  }

  @media (max-width: 1100px) {
    .featured__grid {
      grid-template-columns: 1fr 1fr;
    }
  }

  @media (max-width: 720px) {
    .featured__grid {
      grid-template-columns: 1fr;
    }
  }
</style>