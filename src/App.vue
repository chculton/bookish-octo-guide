<script setup lang="ts">
	import { RouterView } from 'vue-router';
	import NavBar from './components/NavBar.vue';
	import Footer from './components/Footer.vue';

	console.log('Hey dev! Thanks for looking in the console.');
</script>

<template>
	<!-- Hey dev! Thanks for looking in the html. If you're
		interested in the site design, this entire site is
		in a public repo on my GitHub. -->
	<NavBar />

	<RouterView />

	<Footer />
</template>
