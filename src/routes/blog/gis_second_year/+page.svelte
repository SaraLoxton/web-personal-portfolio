<script>
	import Header from "$lib/Header.svelte";
</script>

<section class="hero home-hero">
	<div class="hero-content">
		<Header title="My Year in GIS: What I Learned, Built, and Discovered" subtitle="" />
	</div>
</section>

<section class="section blog-post">
    <div class="container">
        <p class="subtitle is-5">
            December 2025 · 7-8 min read · GIS & Spatial Analysis
        </p>
        <h2 class="title is-4">Introduction</h2>
		<p>
            Over the past year, I’ve worked through a huge range of GIS, remote sensing, cartography, and spatial analysis projects—both through university assignments and my own curiosity. This post brings everything together: what I learned, which tools I used, and the skills that shaped my development as a spatial data scientist.
        </p>
        
        <hr>

        <h2 class="title is-4">Getting Started: Building Core GIS Foundations</h2>
        <p>
            My year began with the fundamentals—learning how to navigate ArcGIS Pro, QGIS, and working through labs focused on spatial thinking. These early assignments helped me understand why spatial problems require a different mindset: scale, projections, coordinate systems, spatial resolution, and how the same dataset can look completely different depending on the choices you make.
        </p>
        <p>I also got familiar with basic GIS workflows:</p>
        <ul>
            <li>Cleaning and organising spatial datasets</li>
            <li>Creating clear, meaningful maps</li>
            <li>Working with attribute tables and symbology</li>
            <li>Understanding vector vs raster differences in practice</li>
        </ul>
        <p>These early tasks set the stage for everything that followed.</p>

        <hr>

        <h2 class="title is-4">Remote Sensing: Seeing Landscapes in a New Way</h2>
        <p>Remote sensing was one of the biggest turning points of the year. For the first time, I wasn’t just using imagery, I was interpreting it, processing it, and extracting meaning from the pixels.</p>
        <p>Some of the key things I worked on:</p>
        <ul>
            <li>Calculating NDVI and understanding vegetation health</li>
            <li>Applying DOS atmospheric correction</li>
            <li>Working with Landsat 5, 7, and 8 imagery</li>
            <li>Creating DEMs and hillshades</li>
            <li>Performing supervised and unsupervised classification</li>
        </ul>
        <p>These assignments taught me how to look at landscapes in ways you can’t see with the naked eye. It also pushed my Python skills further through geospatial libraries like rasterio, NumPy, and Earth Engine.</p>

        <hr>

        <h2 class="title is-4">Spatial Analysis & Modelling: Thinking Beyond the Map</h2>
        <p>Later in the year, the work shifted toward analysis, not just visualisation. This was where GIS started to feel powerful, when you can actually answer questions using spatial data.</p>
        <p>Some of my key learning moments:</p>
        <ul>
            <li>Understanding spatial autocorrelation</li>
            <li>Pattern detection and cluster analysis</li>
            <li>Buffering, overlay analysis, and suitability modelling</li>
            <li>Comparing hemispheric river discharge patterns</li>
            <li>Comparing hemispheric river discharge patterns</li>
            <li>Exploring climate systems and atmospheric circulation</li>
        </ul>
        <p>Many of these assignments weren’t just “do the method.” They required interpretation, storytelling, and explaining why the spatial patterns mattered.</p>

        <hr>

        <h2 class="title is-4">Python, R, and Statistical Workflows</h2>
        <p>A huge part of my growth came from using Python and R with spatial datasets.</p>
        <h2 class="title is-5">In R, I worked on:</h2>
        <ul>
            <li>Data wrangling with tidyverse</li>
            <li>Exploratory analysis of medium-priority lands (Prairie Pothole dataset)</li>
            <li>Modelling (e.g., logistic regression for lizard/chase datasets)</li>
            <li>Handling spatial data with sf</li>
        </ul>
        <h2 class="title is-5">In Python, I expanded into:</h2>
        <ul>
            <li>Raster manipulation with rasterio</li>
            <li>Working with Earth Engine</li>
            <li>Automating workflows</li>
            <li>Building reproducible notebooks for spatial statistics</li>
        </ul>
        <p>
            Learning to move between GIS software and coding tools gave me confidence in adapting to different environments, something essential in real-world spatial work.
        </p>

        <hr>

        <h2 class="title is-4">Cartography & Communication: Making Maps That Mean Something</h2>
        <p>I learned quickly that a “good map” is not the same as a “pretty map.”</p>
        <p>Some of the biggest lessons:</p>
        <ul>
            <li>Always design with a purpose, don’t decorate</li>
            <li>Use hierarchy and colour intentionally</li>
            <li>Labeling can make or break readability</li>
            <li>Captions matter (and should tell the reader what to look for)</li>
        </ul>
        <p>These skills carried over into my portfolio, my assignments, and even the way I present data in non-GIS work.</p>

        <hr>

        <h2 class="title is-4">Major Projects That Shaped My Year</h2>
        <p>
            Here are a few standout projects that pulled everything together:
        </p>
        <h2 class="title is-5">Glacial Retreat in the Southern Alps (Group Project)</h2>
        <p>A multi-layer analysis using DEMs, landcover, and satellite imagery to examine glacial change over time. This taught me how to organise team workflows, choose the right data sources, and communicate results visually.</p>
        <h2 class="title is-5">Spatial Statistics Notebook</h2>
        <p>A fully reproducible Python + R analysis combining statistical modelling with spatial insights.</p>
        <h2 class="title is-5">3D Viewshed & Site Selection</h2>
        <p>Using ArcGIS Pro to simulate visibility and terrain constraints, and building a suitability model integrating weighted layers.</p>
        <p>Each of these helped me develop the ability to choose the right tool for each task, not forcing everything into one software.</p>

        <hr>

        <h2 class="title is-4">Looking Back: What This Year Taught Me</h2>
        <p>More than anything, this year taught me that GIS is a blend of science, art, and storytelling. It requires technical skills, spatial logic, visual clarity, and even creativity.</p>
        <p>My biggest takeaways:</p>
        <ul>
            <li>Spatial problems rarely have one right answer</li>
            <li>Good data cleaning saves hours later</li>
            <li>Clear map design is an essential skill, not an “extra”</li>
            <li>Coding unlocks speed, reproducibility, and deeper analysis</li>
            <li>The best GIS outputs explain why the results matter</li>
        </ul>
        <p>This year pushed me technically and creatively, and I’m excited to continue developing these skills; especially as I move deeper into remote sensing, spatial statistics, and web-based GIS.</p>
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
</style>