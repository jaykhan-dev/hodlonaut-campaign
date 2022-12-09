<script>
	import { fade } from 'svelte/transition';
	import NewLogo from '$lib/images/new-logo.svg';
</script>

<svelte:head>
	<title>Plebeian Market</title>
</svelte:head>

<div transition:fade class="h-screen grid place-items-center bg-white dark:bg-gray-900">
	<div class="grid place-items-center text-black dark:text-white p-4">
		<img src={NewLogo} width={250} alt="Plebeian Market logo" class="my-8" />
		<p class="text-2xl uppercase my-8">Welcome to</p>
		<h1 class="lg:text-8xl text-5xl font-black text-center">Plebeian market</h1>
		<a href="/campaign/hodlonaut" class="my-8 text-2xl btn btn-primary">Hodlonaut Campaign</a>
	</div>
</div>
