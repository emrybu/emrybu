<script lang="ts">
	import Footer from '$lib/components/layout/footer/Footer.svelte';
	import Header from '$lib/components/layout/header/Header.svelte';
	import '$lib/styles/global.css';
	let { children } = $props();
</script>

<svelte:head>
	<link rel="icon" type="image/png" href="/favicon-96x96.png" sizes="96x96" />
	<link rel="icon" type="image/svg+xml" href="/favicon.svg" />
	<link rel="shortcut icon" href="/favicon.svg" />
	<link rel="apple-touch-icon" sizes="180x180" href="/apple-touch-icon.png" />
	<meta name="apple-mobile-web-app-title" content="Emrybu - Доставка суші в Києві" />
	<link rel="manifest" href="/site.webmanifest" />
	<title>Emrybu - Доставка суші в Києві</title>
</svelte:head>

<Header />
{@render children()}
<Footer />
