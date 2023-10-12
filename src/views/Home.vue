<script setup lang="ts">
	import Card from '../components/Card.vue';
</script>

<template>
	<main>
		<div>
			<h2>Alaska-based software and game development</h2>
		</div>

		<Card>
			<template #picture>
				<img src="/TFSCItchioStorefront1.png" />
			</template>
			<template #title><h3>Itch.io Storefront</h3></template>
			<template #card-content
				>We have not released any games yet, though we will be talking about
				upcoming project on this site shortly!</template
			>
		</Card>
	</main>
</template>

<style>
	div {
		margin-bottom: 1rem;
	}
</style>
