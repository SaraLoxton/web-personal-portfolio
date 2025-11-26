<script>
	import Nav from "../../lib/Nav.svelte";
	import Footer from "../../lib/Footer.svelte";

	const experience = [
		{
			role: "Spatial Data Science Student",
			company: "University of Canterbury",
			location: "Christchurch, NZ",
			period: "2023 – Present",
			description:
				"Coursework and projects in GIS, remote sensing, statistics, and algorithms, with a focus on environmental applications.",
			tags: ["GIS", "Remote Sensing", "Data Science"]
		},
		{
			role: "Waitress & Kitchenhand",
			company: "Kohan Restaurant",
			location: "Lake Tekapo, NZ",
			period: "2020 – Present (seasonal)",
			description:
				"Customer service, coordination during peak tourist seasons, and efficient teamwork in a fast-paced environment.",
			tags: ["Customer Service", "Teamwork"]
		},
		{
			role: "Website & Social Media Assistant",
			company: "Tekapo Trails",
			location: "Lake Tekapo, NZ",
			period: "2022",
			description:
				"Set up and managed a simple web presence and social content to promote local trails and community events.",
			tags: ["Web", "Communication"]
		},
        {
			role: "Waitress & Bartender",
			company: "Blue Lake, Eatery & Bar",
			location: "Lake Tekapo, NZ",
			period: "2021 – 2022",
			description:
				"Delivered professional service in a fast-paced hospitality environment. Gained experience with mixology and customer engagement.",
			tags: ["Customer Service", "Teamwork"]
		},
	];

	const education = [
		{
			title: "BSc – Spatial Data Science",
			org: "University of Canterbury",
			location: "Christchurch, NZ",
			period: "2023 – Present",
			description:
				"Combining geography, computer science, and statistics to work with spatial data, maps, and environmental problems."
		},
		{
			title: "Secondary School",
			org: "Craighead Diocean School",
			location: "Timaru, NZ",
			period: "Completed 2023",
			description:
				"Strong foundation in science, and digital technologies."
		}
	];

	const certificates = [
		{
			name: "Bill Apes Memorial Grant",
			issuer: "Tekapo Lions",
			year: "2023",
			description:
				"Support for studies in spatial data science and ongoing volunteering contribution to the local community."
		},
		{
			name: "Microsoft Applied Skills Certificate (Planned)",
			issuer: "Microsoft",
			year: "Online, In Progress",
			description:
				"Developing practical skills in data modelling, dashboards, and cloud-based data workflows."
		}
	];
</script>

<section class="section resume-page">
	<div class="container">
		<header class="resume-header">
			<p class="resume-kicker">Resume &amp; Certificates</p>
			<h1 class="title is-2 resume-title">Overview</h1>
			<p class="subtitle is-5 resume-subtitle">
				A quick snapshot of my experience, education, and certifications. For a full CV,
				feel free to contact me.
			</p>
		</header>

		<div class="columns is-variable is-8 resume-columns">
			<!-- LEFT: Experience -->
			<div class="column is-6">
				<h2 class="resume-section-title">Experience</h2>

				{#each experience as job}
					<article class="resume-item">
						<div class="resume-thumb">
							<span class="resume-thumb-initials">SL</span>
						</div>

						<div class="resume-item-body">
							<h3 class="resume-item-title">{job.role}</h3>
							<p class="resume-item-meta">
								{job.company} · {job.location}
							</p>
							<p class="resume-item-period">{job.period}</p>
							<p class="resume-item-description">
								{job.description}
							</p>

							{#if job.tags}
								<div class="tags resume-tags">
									{#each job.tags as tag}
										<span class="tag is-light resume-tag">{tag}</span>
									{/each}
								</div>
							{/if}
						</div>
					</article>
				{/each}
			</div>

			<!-- RIGHT: Education & Certificates -->
			<div class="column is-6">
				<h2 class="resume-section-title">Education</h2>

				{#each education as edu}
					<article class="resume-item">
						<div class="resume-thumb">
							<span class="resume-thumb-icon">🎓</span>
						</div>

						<div class="resume-item-body">
							<h3 class="resume-item-title">{edu.title}</h3>
							<p class="resume-item-meta">
								{edu.org} · {edu.location}
							</p>
							<p class="resume-item-period">{edu.period}</p>
							<p class="resume-item-description">
								{edu.description}
							</p>
						</div>
					</article>
				{/each}

				<h2 class="resume-section-title resume-section-title--spaced">
					Certifications &amp; Awards
				</h2>

				{#each certificates as cert}
					<article class="resume-item">
						<div class="resume-thumb">
							<span class="resume-thumb-icon">✔</span>
						</div>

						<div class="resume-item-body">
							<h3 class="resume-item-title">{cert.name}</h3>
							<p class="resume-item-meta">
								{cert.issuer}
							</p>
							<p class="resume-item-period">{cert.year}</p>
							<p class="resume-item-description">
								{cert.description}
							</p>
						</div>
					</article>
				{/each}
			</div>
		</div>
	</div>
</section>

<style>
	.resume-page {
		background-color: #f5f3ec;
		min-height: 100vh;
		padding-top: 5rem;
		padding-bottom: 4rem;
	}

	.resume-header {
		margin-bottom: 2.5rem;
	}

	.resume-kicker {
		text-transform: uppercase;
		font-size: 0.8rem;
		font-weight: 600;
		letter-spacing: 0.12em;
		color: #6b6b6b;
	}

	.resume-title {
		color: #1e1f20;
		margin-bottom: 0.2rem;
	}

	.resume-subtitle {
		max-width: 46rem;
		color: #444;
	}

	.resume-section-title {
		font-size: 1rem;
		text-transform: uppercase;
		letter-spacing: 0.14em;
		color: #6b6b6b;
		margin-bottom: 0.75rem;
	}

	.resume-section-title--spaced {
		margin-top: 2rem;
	}

	/* Two column divider */
	.resume-columns {
		position: relative;
	}

	.resume-columns::before {
		content: "";
		position: absolute;
		top: 0.4rem;
		bottom: 0.4rem;
		left: 50%;
		width: 1px;
		background: rgba(0, 0, 0, 0.12);
		transform: translateX(-0.5px);
	}

	/* Cards */
	.resume-item {
		display: flex;
		gap: 1.25rem;
		align-items: flex-start;
		background-color: #fbfaf5;
		border-radius: 16px;
		padding: 1.25rem 1.5rem;
		box-shadow: 0 8px 18px rgba(0, 0, 0, 0.06);
		border: 1px solid rgba(0, 0, 0, 0.04);
		margin-bottom: 1.5rem;
		transition: transform 140ms ease-out, box-shadow 140ms ease-out,
			border-color 140ms ease-out;
	}

	.resume-item:hover {
		transform: translateY(-3px);
		box-shadow: 0 14px 26px rgba(0, 0, 0, 0.1);
		border-color: rgba(63, 83, 35, 0.4);
	}

	.resume-thumb {
		min-width: 64px;
		height: 64px;
		border-radius: 12px;
		background-color: #e2e0d8;
		display: flex;
		align-items: center;
		justify-content: center;
	}

	.resume-thumb-initials,
	.resume-thumb-icon {
		font-weight: 700;
		color: #3f5323;
		font-size: 1.15rem;
	}

	.resume-item-body {
		flex: 1;
	}

	.resume-item-title {
		color: #1e1f20;
		margin-bottom: 0.1rem;
	}

	.resume-item-meta {
		font-size: 0.9rem;
		color: #555;
		margin-bottom: 0.15rem;
	}

	.resume-item-period {
		font-size: 0.85rem;
		color: #777;
		margin-bottom: 0.5rem;
	}

	.resume-item-description {
		font-size: 0.95rem;
		color: #333;
		line-height: 1.5;
	}

	.resume-tags {
		margin-top: 0.6rem;
	}

	.resume-tag {
		border-radius: 999px;
		background-color: #3f5323;
		color: #f7f5ee;
		font-size: 0.75rem;
		font-weight: 600;
	}

	@media screen and (max-width: 768px) {
		.resume-page {
			padding-top: 4rem;
		}

		.resume-columns::before {
			display: none; /* hide vertical divider on mobile */
		}

		.resume-item {
			padding: 1.1rem 1.25rem;
		}
	}
</style>
