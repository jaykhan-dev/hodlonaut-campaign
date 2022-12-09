<script>
	import { fade } from 'svelte/transition';
	import NewLogo from '$lib/images/new-logo.svg';
</script>

<div transition:fade class="h-screen grid place-items-center bg-white dark:bg-gray-900">
	<div class="grid place-items-center">
		<img src={NewLogo} width={400} alt="Plebeian Market logo" class="my-8" />
		<p class="text-2xl uppercase my-8">Welcome to</p>
		<h1 class="lg:text-8xl text-6xl font-black">Plebeian market</h1>
	</div>
</div>
