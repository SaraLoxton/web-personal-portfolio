<script>
  import SectionHeading from '$lib/components/ui/SectionHeading.svelte';
  import { skillGroups } from '$lib/data/skills';
</script>

<section class="skills section" id="skills">
  <div class="container">
    <SectionHeading
      eyebrow="Skills"
      title="Tools and systems I work with"
      description="A mix of geospatial, data, and development tools that support the projects I build."
    />

    <div class="skills__grid">
      {#each skillGroups as group}
        <article class="skills__card">
          <h3>{group.title}</h3>
          <p>{group.description}</p>

          <div class="skills__tags">
            {#each group.items as item}
              <span>{item}</span>
            {/each}
          </div>
        </article>
      {/each}
    </div>
  </div>
</section>

<style lang="scss">
  .skills {
    background:
      linear-gradient(180deg, #0b1220 0%, #0f172a 100%);
  }

  .skills__grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 1.5rem;
    margin-top: 3rem;
  }

  .skills__card {
    padding: 1.75rem;
    border-radius: 1.5rem;
    background: rgba(15, 23, 42, 0.78);
    border: 1px solid rgba(148, 163, 184, 0.14);
  }

  .skills__card h3 {
    margin: 0 0 0.75rem;
    color: #f8fafc;
    font-size: 1.15rem;
  }

  .skills__card p {
    margin: 0 0 1.2rem;
    color: #94a3b8;
    line-height: 1.65;
  }

  .skills__tags {
    display: flex;
    flex-wrap: wrap;
    gap: 0.7rem;
  }

  .skills__tags span {
    display: inline-flex;
    align-items: center;
    padding: 0.55rem 0.85rem;
    border-radius: 999px;
    background: rgba(30, 41, 59, 0.95);
    border: 1px solid rgba(148, 163, 184, 0.15);
    color: #cbd5e1;
    font-size: 0.92rem;
  }

  @media (max-width: 1000px) {
    .skills__grid {
      grid-template-columns: 1fr;
    }
  }
</style>