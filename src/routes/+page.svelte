<script>
	import Header from "../lib/Header.svelte";
	import Footer from "../lib/Footer.svelte";
	import Nav from "../lib/Nav.svelte";
	import Image from "../lib/Image.svelte";
</script>

<!-- Universal Navigation -->
<Nav />

<!-- Main Hero/Header Section -->
<section class="hero">
	<div class="hero-content">
		<Header title="Sara Loxton" subtitle="Spatial Data Scientist & Developer" />
	</div>
</section>

<!-- Featured Section / Introduction -->
<section class="intro-section">
	<div class="intro-grid">
		<!-- Placeholder image component -->
		<div class="intro-image">
			<img src="/favicon.png" alt="Logo placeholder" class="home-logo" />
		</div>

		<!-- Text block -->
		<div class="intro-text">
			<h2>About Me</h2>
			<p>
				I'm Sara, a spatial data science student with a passion for making data visual and meaningful. 
				This website is my personal portfolio—feel free to explore my projects, blog posts, and certifications.
			</p>
		</div>
	</div>
</section>

<!-- Footer -->
<Footer />


<style>
	.home-logo {
		width: 200px;
		height: auto;
		margin: 2rem auto;
		display: block;
	}

</style>