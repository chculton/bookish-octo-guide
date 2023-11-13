<script setup lang="ts">
	import Card from '../components/Card.vue';

	function handleCardClick(linkToGoTo: string) {
		window.open(linkToGoTo);
	}
</script>

<template>
	<main>
		<div>
			<h2>Alaska-based software and game development</h2>
		</div>

		<Card
			@click="handleCardClick('https://github.com/users/chculton/projects/2')"
		>
			<template #picture>
				<img src="/TFSC_VC_IssueTracker1.png" />
			</template>
			<template #title><h3>Velho: Colosseum</h3></template>
			<template #card-content
				>Velho: Colosseum is an upcoming fantasy roguelite. The game's
				development is tracked through issues on the repo's project page. If
				you'd like to follow development, give feedback, or chat with me
				regarding it's progress or potential features, please reach out to me
				anytime through our "About" page.</template
			>
		</Card>

		<Card @click="handleCardClick('https://tundrafeedandsupplyco.itch.io/')">
			<template #picture>
				<img src="/TFSCItchioStorefront1.png" />
			</template>
			<template #title><h3>Itch.io Storefront</h3></template>
			<template #card-content
				>We have not released any games yet, though we will be talking about our
				upcoming projects on this site shortly!</template
			>
		</Card>
	</main>
</template>

<style>
	div {
		margin-bottom: 1rem;
	}
</style>
