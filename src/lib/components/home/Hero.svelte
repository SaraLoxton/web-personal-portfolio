<script>
  import Button from '$lib/components/ui/Button.svelte';
</script>

<section class="hero">
  <div class="hero__inner container">
  <!-- Seperated this block so that the rgb back lighting doesnt get altered by text css -->
    <div class="hero__content">
      <!-- <p class="hero__eyebrow">Spatial Data Science • GIS • Development</p>  Add this back in for the typing thing-->
      <h1>
        Sara
      </h1>
      <p class="hero__subtitle">
        Building spatial data tools, maps, and digital systems that turn information into
        real-world decisions.
      </p>

      <div class="hero__actions">
        <Button href="#featured-projects" variant="primary">View Projects</Button>
        <Button href="#about" variant="secondary">About Me</Button>
      </div>
    </div>
  </div>
</section>

<style lang="scss">
  /* Full Hero section, layer gradient section */
  .hero {
    position: relative;
    min-height: 100svh;
    display: flex;
    align-items: center;
    isolation: isolate;
    background:
      radial-gradient(circle at 20% 20%, rgba(96, 165, 250, 0.12), transparent 30%),
      radial-gradient(circle at 80% 30%, rgba(52, 211, 153, 0.08), transparent 28%),
      linear-gradient(180deg, #08111f 0%, #0b1220 48%, #0f172a 100%);
    overflow: hidden;
    border-bottom: 1px solid rgba(148, 163, 184, 0.12);
  }

  /* Content above the gradient section */
  .hero__inner {
    position: relative;
    z-index: 2;
    width: 100%;
    padding-top: 4rem;
    padding-bottom: 5rem;
  }

  /* Main content */
  .hero__content {
    max-width: 50rem;
    margin-left: 0;
    margin-right: auto;
    text-align: left;
    animation: fadeUp 0.85s ease both;
  }

  h1 {
    margin: 0;
    font-size: clamp(3rem, 8vw, 6.5rem);
    line-height: 0.95;
    letter-spacing: -0.04em;
    color: #f8fafc;
  }

  /* Hero discription section */
  .hero__subtitle {
    margin: 1.5rem 0 0;
    max-width: 42rem;
    font-size: clamp(1.05rem, 2vw, 1.35rem);
    line-height: 1.75;
    color: #cbd5e1;
  }

  .hero__actions {
    display: flex;
    flex-wrap: wrap;
    gap: 1rem;
    margin-top: 2rem;
  }

  @keyframes fadeUp {
    from {
      opacity: 0;
      transform: translateY(22px);
    }
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }

  @media (max-width: 768px) {
    .hero__inner {
      padding-top: 6.5rem;
      padding-bottom: 4rem;
    }

    .hero__subtitle {
      line-height: 1.6;
    }

    .hero__meta {
      gap: 0.7rem;
    }

    .hero__meta span {
      font-size: 0.88rem;
      padding: 0.65rem 0.9rem;
    }
  }
</style>