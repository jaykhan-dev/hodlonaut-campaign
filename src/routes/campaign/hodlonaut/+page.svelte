<script lang="ts">
	import { fade } from 'svelte/transition';
	import Auctions from './Auctions.svelte';
	import Banner from '$lib/images/banner-100.jpg';
</script>

<svelte:head>
	<title>Hodlonaut Campaign</title>
	<meta name="services" content="Services SEO" />
	<script src="https://unpkg.com/@lottiefiles/lottie-player@latest/dist/lottie-player.js"></script>
</svelte:head>

<!-- HERO2-->
<div transition:fade id="bgTwo" class="bg-fixed">
	<div
		class="bg-gradient-to-b from-black/20 to-gray-900 w-full h-full py-20 grid place-items-center"
	>
		<div class="hero-content text-white">
			<div class="grid lg:grid-cols-2">
				<div>
					<h1 class="text-8xl font-bold">Hodlonaut</h1>

					<p class="my-4">
						Whilst we can celebrate Hodlonaut's win in Oslo, the legal battle continues. The British
						legal process is a much bigger event in both time and money.
					</p>
					<p class="my-4">
						This campaign is to provide the Bitcoin community with a perpetual fund raising
						capability whereby anyone can raise money by selling anything physical or their time for
						either a fixed price or an auction (within the laws of the UK).
					</p>
					<div class="flex space-x-4 my-8">
						<button class="btn btn-primary">Auction 1-hour</button>
						<button class="btn btn-secondary">Auction Item</button>
						<button class="btn btn-outline">Fixed Price</button>
					</div>
				</div>
				<!-- LOTTIE -->
				<div class="grid place-items-center">
					<lottie-player
						src="https://assets2.lottiefiles.com/packages/lf20_rmizwv6a.json"
						background="transparent"
						speed="1"
						loop
						autoplay
						class="opacity-40"
						style="width: 400px; height: 400px"
					/>
				</div>
			</div>
		</div>
	</div>
</div>

<!-- Banner -->
<div class="bg-white dark:bg-gray-900 grid place-items-center">
	<img src={Banner} alt="Hodlonaut Banner" width="1280" />
</div>

<div class="grid place-items-center relative bg-white dark:bg-gray-900">
	<h1 class="text-6xl my-8">Get in touch!</h1>
	<div class="lg:flex lg:space-x-4">
		<a
			href="https://defendingbtc.com"
			class="btn btn-outline"
			rel="noopener noreferrer"
			target="_blank">@defendingbtc</a
		>
		<a
			href="https://twitter.com/hodlonaut"
			class="btn btn-outline"
			rel="noopener noreferrer"
			target="_blank">@hodlonaut</a
		>
		<a
			href="https://www.citadel21.com/"
			class="btn btn-outline"
			rel="noopener noreferrer"
			target="_blank">@citadel21</a
		>
	</div>
</div>

<Auctions />

<style>
	#bgTwo {
		background-image: url('../../../lib/images/moon-landscape.jpg');
		background-repeat: no-repeat;
		background-size: cover;
		background-position: center;
		height: 650px;
	}
</style>
