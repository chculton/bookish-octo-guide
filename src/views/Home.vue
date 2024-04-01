<script setup lang="ts">
	import Card from '../components/Card.vue';

	function handleCardClick(linkToGoTo: string) {
		window.open(linkToGoTo);
	}
</script>

<template>
	<main>
		<div class="header">
			<h2>Alaska based software and game development</h2>
		</div>

		<div class="frame">
			<iframe
				width="560"
				height="315"
				src="https://www.youtube.com/embed/um0zp7zBbt4?si=5VPa3FeA77Ccg0ge"
				title="Tundra Feed and Supply Co Channel"
				frameborder="0"
				allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
				referrerpolicy="strict-origin-when-cross-origin"
				allowfullscreen
			></iframe>
		</div>

		<div class="frame">
			<iframe
				frameborder="0"
				src="https://itch.io/embed/2614907?border_width=0&amp;bg_color=000000&amp;fg_color=ffffff&amp;link_color=98fa5b&amp;border_color=bebebe"
				width="560"
				height="165"
				><a href="https://tundrafeedandsupplyco.itch.io/moonwalk-resurgence"
					>Moonwalk: Resurgence by Tundra Feed and Supply Company</a
				></iframe
			>
		</div>

		<Card
			@click="handleCardClick('https://github.com/users/chculton/projects/2')"
		>
			<template #picture>
				<img
					src="/TFSC_VC_IssueTracker1.png"
					class="card-picture"
				/>
			</template>
			<template #title><h3>Velho: Colosseum</h3></template>
			<template #card-content>
				Velho: Colosseum is an upcoming fantasy roguelite. The game's
				development is tracked through issues on the repo's project page. If
				you'd like to follow development, give feedback, or chat with me
				regarding it's progress or potential features, please reach out to me
				anytime through our "About" page.
			</template>
		</Card>
	</main>
</template>

<style>
	.header {
		margin-bottom: 1rem;
	}

	.frame {
		display: flex;
		justify-content: center;
		margin-bottom: 1rem;
	}
</style>
