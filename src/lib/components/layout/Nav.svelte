<script>
	import { List, X } from 'phosphor-svelte';

	let isMenuOpen = false;

	function toggleMenu() {
		isMenuOpen = !isMenuOpen;
	}

	function closeMenu() {
		isMenuOpen = false;
	}
</script>


<nav class="navbar" aria-label="main navigation" >
	<div class="navbar-container">
		<!-- Letter Box links to home -->
		<a class="navbar-item logo" href="/" on:click={closeMenu}>
			<h1> S </h1>
		</a>

		<!-- Desktop nav links (hidden on mobile) -->
		<div class="navbar-links is-hidden-touch">
			<a class="navbar-item" href="/"><section>0.</section>ABOUT  <sectionTwo> | </sectionTwo></a>
			<a class="navbar-item" href="/projects"><section>1.</section>SKILLS</a>
			<a class="navbar-item" href="/blog"><section>2.</section>WORK</a>
			<a class="navbar-item" href="/resume"><section>3.</section>PROJECTS</a>
			<a class="navbar-item" href="/resume"><section>4.</section>CONTACT</a>
			<a class="navbar-item" href="/resume"><section>5.</section>RESUME</a>
		</div>

		<!-- Mobile burger icon (hidden on desktop) -->
		<button
			class="icon-toggle is-hidden-desktop"
			on:click={toggleMenu}
			aria-label="menu toggle">
			{#if isMenuOpen}
				<X size="24" color=$light />
			{:else}
				<List size="24" color=$light />
			{/if}
		</button>
	</div>

	<!-- Mobile dropdown nav -->
	{#if isMenuOpen}
		<div class="mobile-menu is-hidden-desktop">
			<a class="navbar-item" href="/" on:click={closeMenu}>Home</a>
			<a class="navbar-item" href="/projects" on:click={closeMenu}>Projects</a>
			<a class="navbar-item" href="/blog" on:click={closeMenu}>Blog</a>
			<a class="navbar-item" href="/resume" on:click={closeMenu}>Resume/Certificates</a>
			<a class="navbar-item" href="/resume" on:click={closeMenu}>Resume/Certificates</a>
			<a class="navbar-item" href="/resume" on:click={closeMenu}>Resume/Certificates</a>
		</div>
	{/if}
</nav>

<style lang="scss">
	h1{
		font-size: clamp(2rem, 2vw, 2rem);
    	color: #f8fafc;
	}

	sectionTwo {
		color: #f8fafc;
	}

	section {
		color: #56a5a1;
	}

	.navbar {
		padding: 0.75rem 1.5rem;
		background: #08111f;

		position: sticky;
		top: 0;
		z-index: 1000;

		width: 100%;

		.navbar-container {
			display: flex;
			align-items: center;
			justify-content: space-between;
			width: 100%;
			
		}

		.navbar-links {
			display: flex;
			gap: 1.5rem;
		}

		.navbar-item {
			font-weight: 600;
			font-family: $body-font;
		}

		.navbar-item:hover {
			background: linear-gradient(135deg, #56a5a1, #65d6fc); 
			-webkit-text-fill-color: transparent; 
			-webkit-background-clip: text;
		}

		.icon-toggle {
			background: none;
			border: none;
			cursor: pointer;
			padding: 0.5rem;
			border-radius: 6px;
		}

		.mobile-menu {
			display: flex;
			flex-direction: column;
			margin-top: 0.5rem;
		}
	}
</style>