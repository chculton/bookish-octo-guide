<script setup lang="ts">
	import { RouterLink } from 'vue-router';
</script>

<template>
	<header>
		<div class="nav">
			<img
				src="/Background.svg"
				class="nav-bar-logo"
			/>

			<nav class="nav-link-area">
				<RouterLink to="/">Home</RouterLink>
				<RouterLink to="/projects">Projects</RouterLink>
				<RouterLink to="/about">About</RouterLink>
			</nav>
		</div>
	</header>
</template>

<style>
	.nav {
		display: flex;
		margin-bottom: 1rem;
	}

	.nav-bar-logo {
		height: auto;
		width: 10rem;
		min-width: 130px;
	}

	.nav-link-area {
		width: 100%;
		font-size: large;
	}

	nav a.router-link-exact-active {
		color: var(--color-text);
	}

	nav a.router-link-exact-active:hover {
		background-color: transparent;
	}

	nav a {
		display: inline-block;
		padding: 0 1rem;
		border-left: 1px solid var(--color-border);
	}

	nav a:first-of-type {
		border: 0;
	}

	nav {
		text-align: center;
		margin-left: -1rem;
		font-size: 1rem;

		padding: 1rem 0;
		margin-top: 1rem;
	}
</style>
