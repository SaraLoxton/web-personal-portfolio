<script>
  import Button from '$lib/components/ui/Button.svelte';
</script>

<section class="contact-cta section">
  <div class="container">
    <div class="contact-cta__card">
      <p class="contact-cta__eyebrow">Get in touch</p>
      <h2>Interested in geospatial systems, data projects, or collaborative work?</h2>
      <p>
        I’m always keen to connect over spatial data, mapping, practical digital tools, and
        opportunities to build work with real-world value.
      </p>

      <div class="contact-cta__actions">
        <Button href="mailto:saraloxton111@gmail.com" variant="primary">Email Me</Button>
        <Button href="https://github.com/SaraLoxton" variant="secondary">GitHub</Button>
        <Button href="https://www.linkedin.com/in/saraloxton/" variant="ghost">LinkedIn</Button>
      </div>
    </div>
  </div>
</section>

<style lang="scss">
  .contact-cta {
    background: #0f172a;
    padding-top: 2rem;
  }

  .contact-cta__card {
    position: relative;
    overflow: hidden;
    padding: 2.5rem;
    border-radius: 2rem;
    background:
      radial-gradient(circle at top right, rgba(96, 165, 250, 0.1), transparent 25%),
      radial-gradient(circle at bottom left, rgba(52, 211, 153, 0.08), transparent 22%),
      linear-gradient(180deg, rgba(15, 23, 42, 0.96), rgba(11, 18, 32, 0.96));
    border: 1px solid rgba(148, 163, 184, 0.14);
    box-shadow: 0 20px 60px rgba(2, 6, 23, 0.3);
  }

  .contact-cta__eyebrow {
    margin: 0 0 0.8rem;
    color: #93c5fd;
    text-transform: uppercase;
    letter-spacing: 0.14em;
    font-weight: 700;
    font-size: 0.8rem;
  }

  .contact-cta__card h2 {
    margin: 0;
    color: #f8fafc;
    font-size: clamp(2rem, 4vw, 3rem);
    line-height: 1.1;
    max-width: 15ch;
  }

  .contact-cta__card p:not(.contact-cta__eyebrow) {
    margin: 1rem 0 0;
    max-width: 44rem;
    color: #cbd5e1;
    line-height: 1.75;
    font-size: 1.02rem;
  }

  .contact-cta__actions {
    display: flex;
    flex-wrap: wrap;
    gap: 1rem;
    margin-top: 2rem;
  }

  @media (max-width: 768px) {
    .contact-cta__card {
      padding: 1.6rem;
      border-radius: 1.5rem;
    }
  }
</style>