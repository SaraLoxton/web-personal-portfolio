<script>
  import Button from '$lib/components/ui/Button.svelte';
  import Nav from '$lib/components/layout/Nav.svelte'
</script>

<section class="hero">
  <div class="hero__inner container">
    <div class="hero__content">
      <!-- <p class="hero__eyebrow">Spatial Data Science • GIS • Development</p>  Add this back in for the typing thing-->
      <h1>
        Sara Loxton
      </h1>
      <p class="hero__subtitle">
        Building spatial data tools, maps, and digital systems that turn information into
        real-world decisions.
      </p>

      <div class="hero__actions">
        <Button href="#featured-projects" variant="primary">View Projects</Button>
        <Button href="#about" variant="secondary">About Me</Button>
      </div>

      <div class="hero__meta">
        <span>Based in New Zealand</span>
        <span>Spatial Data Science Student</span>
        <span>GIS + Data + Web</span>
      </div>
    </div>
  </div>
</section>

<style lang="scss">
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

  .hero__inner {
    position: relative;
    z-index: 2;
    width: 100%;
    padding-top: 4rem;
    padding-bottom: 5rem;
  }

  .hero__content {
    max-width: 48rem;
    animation: fadeUp 0.85s ease both;
  }

  .hero__eyebrow {
    margin: 0 0 1rem;
    color: #93c5fd;
    font-size: 0.82rem;
    letter-spacing: 0.16em;
    text-transform: uppercase;
    font-weight: 700;
  }

  h1 {
    font-size: clamp(3rem, 8vw, 6.5rem);
    color: #f8fafc;
  }

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

  .hero__meta {
    display: flex;
    flex-wrap: wrap;
    gap: 0.85rem;
    margin-top: 2.2rem;
  }

  .hero__meta span {
    padding: 0.7rem 1rem;
    border: 1px solid rgba(148, 163, 184, 0.18);
    background: rgba(15, 23, 42, 0.52);
    color: #cbd5e1;
    border-radius: 999px;
    font-size: 0.92rem;
    backdrop-filter: blur(10px);
  }

  .hero__pattern {
    position: absolute;
    inset: 0;
    z-index: 0;
    opacity: 0.26;
    background-image: url("data:image/svg+xml,%3Csvg width='1600' height='1000' viewBox='0 0 1600 1000' fill='none' xmlns='http://www.w3.org/2000/svg'%3E%3Cg stroke='rgba(255,255,255,0.16)' stroke-width='1.25' stroke-linecap='round'%3E%3Cpath d='M31 154C121 116 215 133 300 94C398 50 476 13 600 31C697 45 756 97 846 122C947 149 1046 129 1135 86C1241 35 1323 37 1434 73C1498 94 1544 92 1577 84'/%3E%3Cpath d='M25 216C124 180 198 204 275 183C383 154 454 95 566 103C653 110 734 153 829 177C920 200 1020 191 1118 146C1221 98 1328 89 1426 117C1493 137 1540 143 1581 131'/%3E%3Cpath d='M9 291C107 246 184 252 273 245C393 235 487 196 599 211C690 223 760 259 848 277C933 295 1037 295 1138 251C1236 209 1329 186 1438 205C1505 217 1552 227 1596 223'/%3E%3Cpath d='M-2 390C115 347 198 333 306 326C415 319 499 301 601 318C705 335 787 389 889 404C985 417 1075 396 1173 355C1267 315 1354 299 1455 315C1512 324 1562 333 1608 337'/%3E%3Cpath d='M-14 497C83 450 185 430 287 430C392 430 493 419 586 441C693 467 761 508 860 523C960 540 1065 530 1162 490C1265 448 1361 432 1456 445C1514 454 1564 464 1617 472'/%3E%3Cpath d='M-29 614C76 570 175 555 281 559C384 563 475 562 583 586C693 611 782 646 879 656C988 667 1075 651 1176 610C1268 572 1370 553 1474 566C1535 573 1586 591 1626 600'/%3E%3Cpath d='M-29 739C75 699 174 685 280 691C393 698 486 702 591 725C698 748 797 783 896 791C1002 799 1105 777 1204 736C1299 696 1401 676 1492 687C1551 694 1593 710 1637 724'/%3E%3Cpath d='M-38 852C55 822 157 811 264 816C372 821 464 832 574 854C688 877 782 912 885 924C1003 937 1103 920 1210 877C1319 832 1418 812 1510 822C1568 829 1612 843 1652 855'/%3E%3C/g%3E%3C/svg%3E");
    background-size: cover;
    background-position: center;
    filter: blur(0.2px);
    transform: scale(1.05);
  }

  .hero__glow {
    position: absolute;
    border-radius: 999px;
    filter: blur(70px);
    z-index: 1;
    opacity: 0.55;
    pointer-events: none;
  }

  .hero__glow--one {
    width: 22rem;
    height: 22rem;
    top: 10%;
    right: -2rem;
    background: rgba(96, 165, 250, 0.16);
  }

  .hero__glow--two {
    width: 18rem;
    height: 18rem;
    bottom: 8%;
    left: -2rem;
    background: rgba(52, 211, 153, 0.12);
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