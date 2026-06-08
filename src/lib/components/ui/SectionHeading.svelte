<script>
  export let eyebrow = '';
  export let title = '';
  export let description = '';
</script>

<div class="section-heading">
  {#if eyebrow}
    <p class="section-heading__eyebrow">{eyebrow}</p>
  {/if}

  <h2>{title}</h2>

  {#if description}
    <p class="section-heading__description">{description}</p>
  {/if}
</div>

<style lang="scss">
  .section-heading {
    max-width: 48rem;
  }

  .section-heading__eyebrow {
    margin: 0 0 0.85rem;
    color: #93c5fd;
    text-transform: uppercase;
    letter-spacing: 0.14em;
    font-size: 0.8rem;
    font-weight: 700;
  }

  h2 {
    margin: 0;
    color: #f8fafc;
    font-size: clamp(2rem, 4vw, 3.35rem);
    line-height: 1.08;
    letter-spacing: -0.03em;
    text-wrap: balance;
  }

  .section-heading__description {
    margin: 1rem 0 0;
    color: #94a3b8;
    line-height: 1.75;
    font-size: 1.02rem;
  }
</style>