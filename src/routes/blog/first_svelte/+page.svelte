<script>
	import Header from "$lib/Header.svelte";
</script>

<section class="hero home-hero">
	<div class="hero-content">
		<Header title="Building My First Svelte Website" subtitle="How I designed and built my first Svelte portfolio website, starting from sketches and Figma mockups all the way to clean, responsive Svelte components." />
	</div>
</section>

<section class="section blog-post">
    <div class="container">
        <p class="subtitle is-5">
            November 2025 · 5 min read · Website Development
        </p>

		<p>
			This website represents a big personal milestone for me: it’s the first full website I’ve built 
			from scratch using <strong>Svelte</strong>, <strong>Bulma</strong>, and custom SCSS. I wanted a place that not only 
			showcased my GIS and data science work, but also reflected who I am as a developer; clean, minimal, 
			and intentional.
		</p>
        
        <br>

		<h2 class="title is-4">Starting with the Design</h2>
		<p>
			Everything began in Figma. I already had a vision for the aesthetic: Forest greens, soft cream tones, 
			and clean spacing. My goal was to make each section feel structured without feeling heavy. I wanted clarity throughout the pages with intentional uses of fonts, while keeping the website a touch better than bland for my first attempt.
		</p>
		<p>
			I created wireframes for the homepage, the blog, and the projects grid. This step helped me understand 
			how users would move through the site and which sections needed more visual weight. Wireframing brought me back to highschool as I heard my teachers words in my ear for Implications, User Considerations, and Conventions.
		</p>

        <br>

		<h2 class="title is-4">Turning Mockups into Components</h2>
		<p>
			With the visual structure laid out, I started building reusable Svelte components:
		</p>

		<ul>
			<li><strong>Nav.svelte</strong> – a responsive navigation bar with a working mobile burger menu</li>
			<li><strong>Header.svelte</strong> – consistent typography and spacing for hero areas</li>
			<li><strong>Image.svelte</strong> – a simple wrapper for responsive image handling</li>
			<li><strong>Footer.svelte</strong> – a clean, minimal footer across all pages</li>
		</ul>

		<p>
			I quickly discovered how satisfying Svelte’s syntax is—reactivity feels natural, and the component 
			structure made organising each page extremely straightforward. Compared to traditional frameworks 
			I’d used before, Svelte made everything feel lightweight and clean.
		</p>

        <br>

		<h2 class="title is-4">Building the Pages</h2>
		<p>
			Once the components were in place, I built the main pages:
		</p>

		<ul>
			<li><strong>Home</strong> – hero section, about section, and colour-themed layout</li>
			<li><strong>Projects</strong> – a responsive grid of dark cards with tags and action buttons</li>
			<li><strong>Blog</strong> – a clean list of posts, each with metadata and a “Read more” link</li>
			<li><strong>Resume/Certificates</strong> – experience, education, and awards using two columns</li>
		</ul>

		<p>
			Each page needed to feel connected but also unique. Using the same colour palette and font styling 
			throughout helped keep everything cohesive. Bulma gave me a great foundation for spacing and layout, 
			while custom CSS made the design feel more personal.
		</p>

        <br>

		<h2 class="title is-4">The Challenges</h2>
		<p>
			Not everything worked perfectly on the first try. The navigation bar—which felt simple at first—ended 
			up being one of the trickiest parts. I wanted a clean desktop layout and a functional mobile menu, and 
			I learned a lot about how Bulma visibility classes interact with Svelte’s conditional rendering.
		</p>
		<p>
			I also had to restructure the routes after I realised the homepage content was showing on every page. 
			This pushed me to understand SvelteKit layouts better, and I now appreciate how powerful 
			<code>+layout.svelte</code> and slotting can be.
		</p>

        <br>

		<h2 class="title is-4">What I Learned</h2>
		<p>
			This project taught me more than just building a website. I learned how to:
		</p>

		<ul>
			<li>Design intentionally using Figma before diving into code</li>
			<li>Use SvelteKit layouts and routing properly</li>
			<li>Build responsive components that feel cohesive</li>
			<li>Fix UI problems with a mix of Bulma utilities and custom SCSS</li>
			<li>Simplify complex features (like navigation) by returning to basics</li>
		</ul>

		<p>
			Most importantly, I realised how much I enjoy front-end development. There’s something incredibly 
			rewarding about taking an idea from a blank screen, shaping it in Figma, and slowly watching it come 
			to life through code.
		</p>

        <br>

		<h2 class="title is-4">What’s Next?</h2>
		<p>
			Now that the core website is finished, I plan to:
		</p>

		<ul>
			<li>Add more blog posts about GIS, development, and problem-solving</li>
			<li>Expand the Projects page with real-world case studies</li>
			<li>Create a “Version 2” of the design once I gain more experience</li>
			<li>Experiment with motion effects using Svelte transitions</li>
		</ul>

		<p>
			This website represents the start of something bigger—my journey into becoming a spatial data scientist 
			with strong development skills. I’m excited to keep learning and pushing myself, one project at a time.
		</p>

	</div>
</section>

<style>
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

	.blog-post {
		background-color: #f5f3ec;
		padding-top: 4rem;
		padding-bottom: 4rem;
		color: #1a1a1a;
	}

	.blog-post h2 {
		color: #1a1a1a;           
	}

	.subtitle {
		color: #444;
		margin-bottom: 2rem;
	}

	.blog-post p,
	.blog-post li {
		color: #1a1a1a;
		line-height: 1.6;
		margin-bottom: 1.25rem;
	}

	.blog-post ul {
		margin-bottom: 1.25rem;
		padding-left: 1.25rem;
	}

    strong {
    font-weight: bold;
    color: #1a1a1a;   
    }
</style>