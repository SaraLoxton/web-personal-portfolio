<script>
	import Header from "../../lib/Header.svelte";
	import Footer from "../../lib/Footer.svelte";
	import Nav from "../../lib/Nav.svelte";
	import Image from "../../lib/Image.svelte";

const projects = [
    {
	name: "Flat Finder",
      summary:
        "A Svelte-based guide for first-time renters that explains each step of getting a flat.",
      tags: ["Svelte", "JavaScript", "Bulma"],
      links: {
        live: "#",
        code: "#"
      }
    },
    {
      name: "Lake Tekapo Tourism Map",
      summary:
        "Interactive web map showcasing local highlights using Leaflet and spatial data.",
      tags: ["GIS", "Leaflet", "JavaScript"],
      links: {
        live: "#",
        code: "#"
      }
    },
    {
      name: "Remote Sensing Lab Portfolio",
      summary:
        "Collection of remote-sensing labs, including NDVI, DEMs and supervised classifications.",
      tags: ["Python", "Remote Sensing", "Raster"],
      links: {
        live: "#",
        code: "#"
      }
    },
    {
      name: "Data Story Dashboard",
      summary:
        "A simple dashboard exploring environmental datasets with clear narrative and visuals.",
      tags: ["Data Viz", "Python", "Power BI"],
      links: {
        live: "#",
        code: "#"
      }
    },
    {
      name: "Personal Portfolio",
      summary:
        "This website – built with Svelte, Bulma and custom styling to showcase my work.",
      tags: ["Svelte", "Bulma", "Design"],
      links: {
        live: "#",
        code: "#"
      }
    },
    {
      name: "Spatial Statistics Notebook",
      summary:
        "Reproducible analysis of spatial datasets with R and Python, focusing on workflows.",
      tags: ["R", "Python", "Stats"],
      links: {
        live: "#",
        code: "#"
      }
    }
  ];
</script>



<section class="section projects-page">
  <div class="container">

    <!-- Page header -->
    <header class="projects-header">
      <p class="projects-kicker">Portfolio</p>
      <h1 class="title is-2 projects-title">Projects</h1>
      <p class="subtitle is-5 projects-subtitle">
        A selection of work from my studies and personal projects in spatial data
        science, web development, and data visualisation.
      </p>
    </header>

    <!-- Cards grid -->
    <div class="columns is-multiline">
      {#each projects as project}
        <div class="column is-12-tablet is-6-desktop is-4-widescreen">
          <article class="box project-card">
            <header class="project-card-header">
              <h2 class="title is-4 project-name">{project.name}</h2>
            </header>

            <p class="project-summary">
              {project.summary}
            </p>

            <!-- Tags -->
            <div class="tags project-tags">
              {#each project.tags as tag}
                <span class="tag is-light project-tag">{tag}</span>
              {/each}
            </div>

            <!-- Actions -->
            <div class="project-actions">
              {#if project.links.live}
                <a
                  class="button is-small is-dark is-outlined"
                  href={project.links.live}
                  target="_blank"
                  rel="noreferrer"
                >
                  View project
                </a>
              {/if}

              {#if project.links.code}
                <a
                  class="button is-small is-light"
                  href={project.links.code}
                  target="_blank"
                  rel="noreferrer"
                >
                  View code
                </a>
              {/if}
            </div>
          </article>
        </div>
      {/each}
    </div>
  </div>
</section>


<style>
  /* Page background + spacing – matches your homepage feel */
  .projects-page {
    background-color: #f5f3ec; /* same cream as About section */
    min-height: 100vh;
    padding-top: 5rem; /* clears the navbar */
	padding-bottom: 4rem; 
  }

  .projects-page .container {
  max-width: 1200px;
  }

  .projects-header {
  margin-bottom: 2rem;
  }

  .projects-kicker {
    text-transform: uppercase;
    letter-spacing: 0.12em;
    font-size: 0.8rem;
    font-weight: 600;
    color: #6b6b6b;
  }

  .projects-title {
  color: #1e1f20;
  font-weight: 700;
  margin-bottom: 0.2rem; /* add this so subtitle nests closer */
  }

  .projects-subtitle {
    max-width: 46rem;
    color: #444;
  }

  /* Card styling – inspired by your figma + dark example,
     but lightened to fit with the cream background */
  .project-card {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    height: 100%;
    background-color: #111317; /* dark body of card (like inspiration) */
    color: #f5f5f5;
    border-radius: 10px;
    box-shadow: 0 8px 18px rgba(0, 0, 0, 0.35);
    border: 1px solid rgba(255, 255, 255, 0.04);
	transition: transform 150ms ease-out, box-shadow 150ms ease-out;
  }

  .project-card:hover {
  transform: translateY(-4px);                    
  box-shadow: 0 16px 32px rgba(0, 0, 0, 0.4);
  }

  .project-card-header {
    margin-bottom: 0.5rem;
  }

  .project-name {
    margin-bottom: 0.2rem;
    color: #ffffff;
  }

  .project-summary {
    font-size: 0.95rem;
    color: #d6d6d6;
    margin-bottom: 1rem;
  }

  .project-tags {
    margin-bottom: 1.25rem;
  }

  .project-tag {
  border-radius: 999px;
  padding-inline: 0.75rem;
  padding-block: 0.35rem;
  font-size: 0.8rem;
  font-weight: 600;
  background-color: #3f5323;
  color: #f7f5ee;
  border: 1px solid rgba(255, 255, 255, 0.1);
  }

  .project-tag + .project-tag {
    margin-left: 0.4rem;
  }

  .project-actions {
    display: flex;
    gap: 0.5rem;
    margin-top: auto;
  }

  .project-actions .button.is-dark.is-outlined {
    background-color: transparent;
    border-color: #e1e1e1;
    color: #f5f5f5;
  }

  .project-actions .button.is-dark.is-outlined:hover {
    background-color: #f5f5f5;
    color: #111317;
  }

  .project-actions .button.is-light {
    background-color: #f5f3ec;
    color: #111317;
  }

  .project-actions .button.is-light:hover {
    background-color: #ffffff;
  }

  /* Responsive tweaks */
  @media screen and (max-width: 768px) {
    .projects-page {
      padding-top: 4rem;
    }

    .projects-header {
      text-align: left;
    }
  }
</style>