<script lang="ts">
	import { fade } from 'svelte/transition';

	import Banner from '$lib/images/banner-100.jpg';
	import Tabs from './TabsHodlonaut.svelte';
</script>

<svelte:head>
	<title>Hodlonaut Campaign</title>
	<meta name="services" content="Services SEO" />
	<script src="https://unpkg.com/@lottiefiles/lottie-player@latest/dist/lottie-player.js"></script>
</svelte:head>

<!-- HERO2-->
<div transition:fade id="bgTwo" class="bg-fixed block">
	<div
		class="dark:bg-gradient-to-b dark:from-gray-900/20 dark:to-gray-900 bg-gradient-to-b from-gray-900/20 to-white w-full h-full py-36 grid place-items-center"
	>
		<!-- Banner -->
		<div
			class="bg-white dark:bg-gray-900 grid place-items-center my-8 border rounded border-black dark:border-white/20 shadow-2xl"
		>
			<img src={Banner} alt="Hodlonaut Banner" width="1280" />
		</div>
	</div>
</div>

<!-- ACTION BUTTONS -->
<div class="text-black dark:text-white bg-white dark:bg-gray-900">
	<div class="grid lg:grid-cols-2 gap-10 lg:w-2/3 mx-auto p-2">
		<!-- COL -->
		<div class="">
			<h1 class="lg:text-8xl text-6xl font-bold">Hodlonaut</h1>

			<p class="my-8 leading-10">
				Whilst we can celebrate Hodlonaut's win in Oslo, the legal battle continues. The British
				legal process is a much bigger event in both time and money.
			</p>
			<p class="my-8 leading-10">
				This campaign is to provide the Bitcoin community with a perpetual fund raising capability
				whereby anyone can raise money by selling anything physical or their time for either a fixed
				price or an auction (within the laws of the UK).
			</p>
		</div>

		<!-- COL -->
		<div class="grid relative text-black dark:text-white">
			<div class="">
				<h1 class="uppercase text-xl font-bold my-8">Verify, Don't Trust.</h1>
				<p class="font-bold text-sm">
					Note: all money from the sales in this campaign will go to addresses generated from the
					following XPUB.
				</p>
				<div class="py-4 flex items-center space-x-2">
					<input
						type="text"
						placeholder="xpub6D93ecgDqmNjxsM6hN7Qf5Wxt"
						class="w-full p-3 rounded-md shadow-xl input"
					/>
					<button class="btn btn-outline">Copy XPUB</button>
				</div>
			</div>
			<div class="flex justify-center py-4 border-b border-t dark:border-white/20 border-black/20">
				<a
					href="https://defendingbtc.com"
					class="text-3xl font-bold"
					rel="noopener noreferrer"
					target="_blank">@defendingbtc</a
				>
			</div>
			<div class="grid lg:grid-cols-1 gap-4 my-8">
				<button class="btn btn-primary">Auction 1-hour of your time</button>
				<div class="">
					<p class="text-center">OR</p>
				</div>
				<div class="grid grid-cols-2 gap-4">
					<button class="btn btn-outline">Auction Item</button>
					<button class="btn btn-outline">Sell Item</button>
				</div>
			</div>
		</div>

		<!-- LOTTIE -->
		<div class="grid place-items-center" />
	</div>
</div>

<!-- CONTACT -->

<!-- AUCTIONS -->
<div class="grid place-items-center bg-white dark:bg-gray-900 pt-20 text-black dark:text-white">
	<h1 class="lg:text-8xl text-4xl font-black my-8">Auctions</h1>
</div>
<Tabs />

<style>
	#bgTwo {
		background-image: url('../../../lib/images/moon-landscape.jpg');
		background-repeat: no-repeat;
		background-size: cover;
		background-position: center;
	}
</style>
