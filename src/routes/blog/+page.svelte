<script>
	import Nav from "../../lib/Nav.svelte";
	import Footer from "../../lib/Footer.svelte";

	const posts = [
		{
			title: "Understanding NDVI for Remote Sensing",
			summary:
				"A beginner-friendly explanation of NDVI, how it works, and how to interpret vegetation health using satellite imagery.",
			category: "Remote Sensing",
			date: "March 2025",
			readTime: "6 min read",
			link: "#"
		},
		{
			title: "Building My First Svelte App",
			summary:
				"A walkthrough of the development process behind my Flat Finder app, from wireframes to a fully functional UI.",
			category: "Web Development",
			date: "April 2025",
			readTime: "8 min read",
			link: "#"
		},
		{
			title: "Data Storytelling with Power BI",
			summary:
				"How data storytelling principles guide dashboard design, supported by examples from environmental datasets.",
			category: "Data Visualisation",
			date: "May 2025",
			readTime: "5 min read",
			link: "#"
		}
	];
</script>

<section class="section blog-page">
	<div class="container">
		<header class="blog-header">
			<p class="blog-kicker">Blog</p>
			<h1 class="title is-2 blog-title">Latest Posts</h1>
			<p class="subtitle is-5 blog-subtitle">
				Thoughts, tutorials, and insights on spatial analysis, development, and data
				science.
			</p>
		</header>

		<div class="posts">
			{#each posts as post}
				<article class="post-card">
					<div class="post-content">
						<p class="post-meta">
							<span class="post-chip">{post.category}</span>
							<span class="post-meta-text">{post.date} · {post.readTime}</span>
						</p>

						<h2 class="title is-4 post-title">{post.title}</h2>

						<p class="post-summary">
							{post.summary}
						</p>

						<a class="button is-small is-dark is-outlined post-button" href={post.link}>
							Read more
						</a>
					</div>
				</article>
			{/each}
		</div>
	</div>
</section>

<style>
	.blog-page {
		background-color: #f5f3ec;
		min-height: 100vh;
		padding-top: 5rem;
		padding-bottom: 4rem;
	}

	.blog-header {
		margin-bottom: 2.5rem;
	}

	.blog-kicker {
		text-transform: uppercase;
		font-size: 0.8rem;
		font-weight: 600;
		letter-spacing: 0.12em;
		color: #6b6b6b;
	}

	.blog-title {
		color: #1e1f20;
		margin-bottom: 0.2rem;
	}

	.blog-subtitle {
		max-width: 46rem;
		color: #444;
	}

	.posts {
		display: flex;
		flex-direction: column;
		gap: 1.75rem;
	}

	/* Card */
	.post-card {
		background-color: #fbfaf5;
		border-radius: 16px;
		padding: 1.75rem 2rem;
		box-shadow: 0 8px 18px rgba(0, 0, 0, 0.08);
		border: 1px solid rgba(0, 0, 0, 0.04);
		transition: transform 140ms ease-out, box-shadow 140ms ease-out,
			border-color 140ms ease-out;
	}

	.post-card:hover {
		transform: translateY(-3px);
		box-shadow: 0 14px 26px rgba(0, 0, 0, 0.12);
		border-color: rgba(63, 83, 35, 0.55); /* subtle green accent */
	}

	.post-content {
		max-width: 48rem;
	}

	/* Meta line */
	.post-meta {
		display: flex;
		align-items: center;
		gap: 0.75rem;
		margin-bottom: 0.75rem;
		font-size: 0.85rem;
		color: #666;
	}

	.post-chip {
		background-color: #3f5323;
		color: #f7f5ee;
		padding: 0.2rem 0.8rem;
		border-radius: 999px;
		font-size: 0.75rem;
		font-weight: 600;
		text-transform: uppercase;
		letter-spacing: 0.08em;
	}

	.post-meta-text {
		font-style: italic;
	}

	.post-title {
		color: #1e1f20;
		margin-bottom: 0.35rem;
	}

	.post-summary {
		color: #333;
		margin-bottom: 1.25rem;
		font-size: 1rem;
		line-height: 1.55;
	}

	.post-button {
		border-radius: 999px;
		padding-inline: 1.25rem;
	}

	@media screen and (max-width: 768px) {
		.blog-page {
			padding-top: 4rem;
		}

		.post-card {
			padding: 1.5rem 1.4rem;
		}
	}
</style>
