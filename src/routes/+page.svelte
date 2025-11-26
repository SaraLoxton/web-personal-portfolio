<script>
	// Only need Header here now – Nav and Footer live in +layout.svelte
	import Header from "../lib/Header.svelte";
</script>

<!-- Main Hero/Header Section -->
<section class="hero home-hero">
	<div class="hero-content">
		<Header title="Sara Loxton" subtitle="Spatial Data Scientist & Developer" />
	</div>
</section>

<!-- Featured Section / Introduction -->
<section class="intro-section">
	<div class="intro-grid">
		<!-- Logo / image -->
		<div class="intro-image">
			<img src="/favicon.png" alt="Logo placeholder" class="home-logo" />
		</div>

		<!-- Text block -->
		<div class="intro-text">
			<h2>About Me</h2>
			<p>
				I'm Sara, a spatial data science student with a passion for making data visual
				and meaningful. This website is my personal portfolio – feel free to explore
				my projects, blog posts, and certifications.
			</p>
		</div>
	</div>
</section>

<style>
	/* HERO */

	.home-hero {
		background-color: #3f5323; /* your green */
		color: #f5f3ec;
		padding: 5rem 1.5rem 4rem;
		text-align: center;
	}

	.hero-content {
		max-width: 960px;
		margin: 0 auto;
	}

	/* INTRO */

	.intro-section {
		background-color: #f5f3ec; /* cream band like other pages */
		color: #1e1f20;
		padding: 4rem 1.5rem 5rem;
	}

	.intro-grid {
		max-width: 1100px;
		margin: 0 auto;
		display: grid;
		grid-template-columns: minmax(0, 1fr) minmax(0, 1.4fr);
		gap: 3rem;
		align-items: center;
	}

	.intro-image {
		display: flex;
		justify-content: center;
	}

	.home-logo {
		width: 220px;
		height: auto;
		display: block;
	}

	.intro-text h2 {
		font-size: 1.6rem;
		margin-bottom: 0.75rem;
	}

	.intro-text p {
		font-size: 1rem;
		line-height: 1.6;
		max-width: 34rem;
	}

	/* Responsive */

	@media screen and (max-width: 768px) {
		.home-hero {
			padding-top: 4rem;
			padding-bottom: 3rem;
		}

		.intro-section {
			padding: 3rem 1.25rem 4rem;
		}

		.intro-grid {
			grid-template-columns: 1fr;
			text-align: center;
		}

		.intro-text p {
			margin: 0 auto;
		}
	}
</style>