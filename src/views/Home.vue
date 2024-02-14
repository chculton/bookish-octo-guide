<script setup lang="ts">
	import { onMounted } from 'vue';
	import Card from '../components/Card.vue';

	function handleCardClick(linkToGoTo: string) {
		window.open(linkToGoTo);
	}

	function displayLatestVideo() {
		const cid = 'UC2M7T8BMvOAltQmLRaCphDg';
		const channelURL = encodeURIComponent(
			`https://www.youtube.com/feeds/videos.xml?channel_id=${cid}`
		);

		const frame = document.getElementById('channel') as HTMLIFrameElement;

		fetch(`https://api.rss2json.com/v1/api.json?rss_url=${channelURL}`)
			.then((response) => response.json())
			.then((data) => {
				var guid = data['items'][0]['guid'];
				const embedURL =
					'https://youtube.com/embed/' + guid.replace('yt:video:', '');

				frame.src = embedURL;
			})
			.catch((err) => {
				console.error(err);
			});
	}

	onMounted(() => {
		displayLatestVideo();
	});
</script>

<template>
	<main>
		<div class="header">
			<h2>Alaska based software and game development</h2>
		</div>

		<div class="channel-frame">
			<iframe
				id="channel"
				width="560"
				height="315"
				title="Tundra Feed and Supply Co Channel"
				frameborder="0"
				allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; web-share"
				allowfullscreen
			></iframe>
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

		<Card @click="handleCardClick('https://tundrafeedandsupplyco.itch.io/')">
			<template #picture>
				<img
					src="/TFSCItchioStorefront1.png"
					class="card-picture"
				/>
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
	.header {
		margin-bottom: 1rem;
	}

	.channel-frame {
		display: flex;
		justify-content: center;
		margin-bottom: 1rem;
	}
</style>
