<script>
	import '../app.postcss';
	import Footer from '$lib/components/footer.svelte';
	import Header from '$lib/components/header.svelte';
</script>

<div>
	<Header />

	<main>
		<slot />
	</main>

	<Footer />
</div>
