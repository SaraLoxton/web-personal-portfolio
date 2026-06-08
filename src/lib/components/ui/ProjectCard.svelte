<script>
  export let project;
</script>

<article class="project-card">
  <div class="project-card__image">
    <img src={project.image} alt={project.alt} />
    <div class="project-card__image-overlay"></div>
    <span>{project.label}</span>
  </div>

  <div class="project-card__body">
    <h3>{project.title}</h3>
    <p>{project.description}</p>

    <div class="project-card__tags">
      {#each project.stack as item}
        <span>{item}</span>
      {/each}
    </div>

    <div class="project-card__links">
      {#if project.live && project.live !== '#'}
        <a href={project.live} target="_blank" rel="noreferrer">Live</a>
      {/if}
      {#if project.github && project.github !== '#'}
        <a href={project.github} target="_blank" rel="noreferrer">GitHub</a>
      {/if}
    </div>
  </div>
</article>

<style lang="scss">
  .project-card {
    display: flex;
    flex-direction: column;
    overflow: hidden;
    min-height: 100%;
    border-radius: 1.7rem;
    background: rgba(15, 23, 42, 0.84);
    border: 1px solid rgba(148, 163, 184, 0.14);
    box-shadow: 0 12px 34px rgba(2, 6, 23, 0.22);
    transition:
      transform 0.24s ease,
      border-color 0.24s ease,
      box-shadow 0.24s ease;
  }

  .project-card:hover {
    transform: translateY(-6px);
    border-color: rgba(96, 165, 250, 0.28);
    box-shadow: 0 22px 42px rgba(2, 6, 23, 0.28);
  }

  .project-card__image {
    position: relative;
    min-height: 13rem;
    overflow: hidden;
    border-bottom: 1px solid rgba(148, 163, 184, 0.1);
  }

  .project-card__image img {
    width: 100%;
    height: 100%;
    min-height: 13rem;
    object-fit: cover;
    display: block;
    transition: transform 0.45s ease;
  }

  .project-card:hover .project-card__image img {
    transform: scale(1.04);
  }

  .project-card__image-overlay {
    position: absolute;
    inset: 0;
    background:
      linear-gradient(to top, rgba(8, 17, 31, 0.85), rgba(8, 17, 31, 0.15)),
      linear-gradient(to right, rgba(8, 17, 31, 0.35), transparent 60%);
    pointer-events: none;
  }

  .project-card__image span {
    position: absolute;
    top: 1rem;
    left: 1rem;
    z-index: 2;
    padding: 0.5rem 0.8rem;
    border-radius: 999px;
    background: rgba(15, 23, 42, 0.72);
    border: 1px solid rgba(148, 163, 184, 0.14);
    color: #cbd5e1;
    font-size: 0.85rem;
    backdrop-filter: blur(10px);
  }

  .project-card__body {
    display: flex;
    flex-direction: column;
    gap: 1rem;
    padding: 1.5rem;
  }

  .project-card__body h3 {
    margin: 0;
    color: #f8fafc;
    font-size: 1.25rem;
    line-height: 1.2;
  }

  .project-card__body p {
    margin: 0;
    color: #cbd5e1;
    line-height: 1.7;
  }

  .project-card__tags {
    display: flex;
    flex-wrap: wrap;
    gap: 0.65rem;
  }

  .project-card__tags span {
    padding: 0.45rem 0.72rem;
    border-radius: 999px;
    background: rgba(30, 41, 59, 0.95);
    border: 1px solid rgba(148, 163, 184, 0.14);
    color: #94a3b8;
    font-size: 0.84rem;
  }

  .project-card__links {
    display: flex;
    gap: 1rem;
    margin-top: auto;
    padding-top: 0.5rem;
  }

  .project-card__links a {
    color: #93c5fd;
    text-decoration: none;
    font-weight: 700;
  }

  .project-card__links a:hover {
    color: #f8fafc;
  }
</style>