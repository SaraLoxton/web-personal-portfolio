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

<nav class="navbar is-light" role="navigation" aria-label="main navigation">
	<div class="navbar-container">
		<!-- Logo links to home -->
		<a class="navbar-item logo" href="/" on:click={closeMenu}>
			<img src="/saraLoxtonLogoUpdated.png" alt="Sara Loxton Logo" class="logo-image" />
		</a>

		<!-- Desktop nav links (hidden on mobile) -->
		<div class="navbar-links is-hidden-touch">
			<a class="navbar-item" href="/">Home</a>
			<a class="navbar-item" href="/projects">Projects</a>
			<a class="navbar-item" href="/blog">Blog</a>
			<a class="navbar-item" href="/resume">Resume/Certificates</a>
		</div>

		<!-- Mobile burger icon (hidden on desktop) -->
		<button
			class="icon-toggle is-hidden-desktop"
			on:click={toggleMenu}
			aria-label="menu toggle">
			{#if isMenuOpen}
				<X size="24" color="var(--onyx)" />
			{:else}
				<List size="24" color="var(--onyx)" />
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
		</div>
	{/if}
</nav>

<style lang="scss">
	.logo-image {
		height: 3rem;
		width: auto;
		object-fit: contain;
	}

	.navbar {
		background-color: $secondary;
		color: $primary;
		padding: 0.75rem 1.5rem;

		.navbar-container {
			display: flex;
			align-items: center;
			justify-content: space-between;
			width: 100%;
		}

		.logo {
			font-weight: bold;
			margin-right: auto;
		}

		.navbar-links {
			display: flex;
			gap: 1.5rem;
		}

		.navbar-item {
			font-weight: 600;
			font-family: $body-font;
		}

		.icon-toggle {
			background: none;
			border: none;
			cursor: pointer;
			padding: 0.5rem;
			border-radius: 6px;

			&:hover {
				background-color: rgba(0, 0, 0, 0.05);
			}
		}

		.mobile-menu {
			display: flex;
			flex-direction: column;
			margin-top: 0.5rem;
		}
	}
</style>
