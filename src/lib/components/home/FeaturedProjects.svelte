<script>
  import SectionHeading from '$lib/components/ui/SectionHeading.svelte';
  import ProjectCard from '$lib/components/ui/ProjectCard.svelte';
  import { featuredProjects } from '$lib/data/projects';
</script>

<section class="featured section" id="featured-projects">
  <div class="container">
    <SectionHeading
      eyebrow="Projects"
      title="Selected work that blends data, place, and digital design"
      description="Scroll through a selection of projects covering geospatial analysis, data systems, and digital development."
    />

    <!--
      Horizontal project catalogue.
      tabindex allows keyboard users to focus and scroll the catalogue.
    -->
    <div class="featured__catalogue" tabindex="0" aria-label="Scrollable list of featured projects">
        {#each featuredProjects as project}
        <div class="featured__item">
          <ProjectCard {project} />
        </div>
      {/each}
    </div>

    <!-- Small visual hint that more projects are available to the right. -->
    <div class="featured__hint" aria-hidden="true">
      <span>Scroll for more projects</span>
      <span class="featured__arrow">→</span>
    </div>
  </div>
</section>

<style lang="scss">
  .featured {
    background: #0b1220;
  }

  .featured__catalogue {
    display: grid;
    grid-auto-flow: column;
    grid-auto-columns: minmax(19rem, 24rem);
    gap: 1.5rem;

    margin-top: 3rem;
    padding: 0.25rem 0 1.25rem;

    overflow-x: auto;
    overflow-y: hidden;

    scroll-snap-type: x mandatory;
    scroll-behavior: smooth;
    overscroll-behavior-inline: contain;

    /* Breathing room for the snapping feature */
    scroll-padding-inline: 0.25rem;

    /* Fixing the touch scrolling on mobile */
    -webkit-overflow-scrolling: touch;

    /* Keyboard focus style for accessibility */
    outline: none;
  }

  .featured__catalogue:focus-visible {
    border-radius: 1rem;
    box-shadow: 0 0 0 2px rgba(96, 165, 250, 0.55);
  }

  /* Makes component reuseable everywhere. */
  .featured__item {
    min-width: 0;
    scroll-snap-align: start;
    scroll-snap-stop: always;
  }

  /* Makes every card fill the available catalogue column height */
  .featured__item :global(.project-card) {
    height: 100%;
  }

  /* Text hint shown below the catalogue */
  .featured__hint {
    display: flex;
    align-items: center;
    justify-content: flex-end;
    gap: 0.55rem;

    margin-top: 0.6rem;

    color: #94a3b8;
    font-size: 0.88rem;
    letter-spacing: 0.02em;
  }

  /* Subtle movement makes the direction of scrolling clearer. */
  .featured__arrow {
    color: #60a5fa;
    font-size: 1.2rem;
    animation: moveArrow 1.5s ease-in-out infinite;
  }

  @keyframes moveArrow {
    0%,
    100% {
      transform: translateX(0);
    }

    50% {
      transform: translateX(0.35rem);
    }
  }

  /* Custom horizontal scrollbar for Chromium and Safari browsers */
  .featured__catalogue::-webkit-scrollbar {
    height: 0.55rem;
  }

  .featured__catalogue::-webkit-scrollbar-track {
    background: rgba(15, 23, 42, 0.85);
    border-radius: 999px;
  }

  .featured__catalogue::-webkit-scrollbar-thumb {
    background: rgba(96, 165, 250, 0.45);
    border-radius: 999px;
  }

  .featured__catalogue::-webkit-scrollbar-thumb:hover {
    background: rgba(96, 165, 250, 0.7);
  }

  /* Firefox scrollbar styling. */
  .featured__catalogue {
    scrollbar-width: thin;
    scrollbar-color:
      rgba(96, 165, 250, 0.45)
      rgba(15, 23, 42, 0.85);
  }

  /* Slightly wider cards on large desktop screens  */
  @media (min-width: 1200px) {
    .featured__catalogue {
      grid-auto-columns: minmax(21rem, 26rem);
    }
  }

  /* Showing the next card on smaller screens */
  @media (max-width: 720px) {
    .featured__catalogue {
      grid-auto-columns: minmax(17rem, 84vw);
      gap: 1rem;
    }

    .featured__hint {
      justify-content: flex-start;
    }
  }
</style>

