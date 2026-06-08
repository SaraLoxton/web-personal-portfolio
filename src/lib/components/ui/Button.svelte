<script>
  export let href = '#';
  export let variant = 'primary';
</script>

<a class={`button button--${variant}`} {href}>
  <slot />
</a>

<style lang="scss">
  .button {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    min-height: 3rem;
    padding: 0.9rem 1.25rem;
    border-radius: 999px;
    text-decoration: none;
    font-weight: 700;
    letter-spacing: -0.01em;
    transition:
      transform 0.22s ease,
      background-color 0.22s ease,
      border-color 0.22s ease,
      color 0.22s ease,
      box-shadow 0.22s ease;
  }

  .button:hover {
    transform: translateY(-2px);
  }

  .button--primary {
    background: linear-gradient(135deg, #60a5fa, #34d399);
    color: #08111f;
    box-shadow: 0 14px 30px rgba(52, 211, 153, 0.16);
  }

  .button--primary:hover {
    box-shadow: 0 18px 34px rgba(96, 165, 250, 0.22);
  }

  .button--secondary {
    background: rgba(15, 23, 42, 0.8);
    color: #f8fafc;
    border: 1px solid rgba(148, 163, 184, 0.22);
  }

  .button--secondary:hover {
    border-color: rgba(96, 165, 250, 0.32);
    background: rgba(30, 41, 59, 0.9);
  }

  .button--ghost {
    background: transparent;
    color: #cbd5e1;
    border: 1px solid rgba(148, 163, 184, 0.14);
  }

  .button--ghost:hover {
    color: #f8fafc;
    border-color: rgba(148, 163, 184, 0.28);
    background: rgba(15, 23, 42, 0.58);
  }
</style>