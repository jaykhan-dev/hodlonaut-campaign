<script>
	import '../app.postcss';
	import Footer from '$lib/components/footer.svelte';
	import Header from '$lib/components/header.svelte';
	import { darkTheme } from '../Store';

	$: dark = $darkTheme;
</script>

<div class:dark>
	<Header />

	<main class="">
		<slot />
	</main>

	<Footer />
</div>
