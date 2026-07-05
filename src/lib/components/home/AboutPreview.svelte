<script>
  import SectionHeading from '$lib/components/ui/SectionHeading.svelte';
</script>

<section class="about section" id="about">
  <div class="container">
    <SectionHeading
      eyebrow="About"
      title="Making practical, people-focused approachs to a spatial thinking."
      description="I’m interested in how maps, data, and digital tools can support clearer decisions in environmental, rural, and community settings."
    />

    <div class="about__grid">
      <article class="about__card">
        <h3>Who I am</h3>
        <p>
          I’m a Spatial Data Science third year student at the University of Canterbury with a growing focus
          on GIS, geospatial analysis, data systems, and purposeful digital design.
        </p>
      </article>

      <article class="about__card">
        <h3>What I build</h3>
        <p>
          My work spans mapping, remote sensing, data workflows, and front-end development (Including this website).
          I especially love projects that make technical information easier to understand and use.
        </p>
      </article>

      <article class="about__card">
        <h3>What I care about</h3>
        <p>
          Raised in the Mackenzie Basin, I’m especially drawn to projects connected to land,
          environment, rural systems, and local communities.
          "Takes villagers to become a Village" is my favourite quote that embodies this.
        </p>
      </article>
    </div>
  </div>
</section>

<style lang="scss">
  .about {
    background:
      radial-gradient(circle at 0% 0%, rgba(96, 165, 250, 0.04), transparent 18%),
      #0f172a;
  }

  .about__grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 1.5rem;
    margin-top: 3rem;
  }

  .about__card {
    padding: 1.75rem;
    border-radius: 1.5rem;
    background: rgba(15, 23, 42, 0.72);
    border: 1px solid rgba(148, 163, 184, 0.14);
    box-shadow: 0 10px 30px rgba(2, 6, 23, 0.22);
    transition: transform 0.22s ease, border-color 0.22s ease, box-shadow 0.22s ease;
  }

  .about__card:hover {
    transform: translateY(-4px);
    border-color: rgba(96, 165, 250, 0.28);
    box-shadow: 0 18px 42px rgba(2, 6, 23, 0.28);
  }

  .about__card h3 {
    margin: 0 0 0.9rem;
    color: #f8fafc;
    font-size: 1.15rem;
  }

  .about__card p {
    margin: 0;
    color: #cbd5e1;
    line-height: 1.75;
  }

  @media (max-width: 900px) {
    .about__grid {
      grid-template-columns: 1fr;
    }
  }
</style>