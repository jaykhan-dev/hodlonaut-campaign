<script>
	import SpaceCat from '$lib/images/space-cat.png';

	// let date = new Date()
</script>

<svelte:head>
	<script src="https://unpkg.com/@lottiefiles/lottie-player@latest/dist/lottie-player.js"></script>
</svelte:head>

<div class="bg-white dark:bg-gray-900 text-black dark:text-white">
	<div class="grid place-items-center text-center p-4">
		<!-- <div class="tabs tabs-boxed">
      <a class="tab">Tab 1</a>
      <a class="tab">Tab 2</a>
      <a class="tab">Tab 3</a>
    </div> -->

		<div class="">
			<!-- CARD -->
			<div class="grid lg:grid-cols-3 border border-white/20">
				<figure class="grid place-items-center p-2"><img src={SpaceCat} alt="space cat" /></figure>
				<div class="lg:col-span-2 p-4">
					<div
						class="lg:flex items-center justify-between border p-2 rounded border-white/20 bg-green-300 text-black"
					>
						<div class="flex items-center justify-center space-x-4 my-2">
							<div class="avatar">
								<div
									class="w-12 h-12 rounded-full ring ring-primary ring-offset-base-100 ring-offset-2"
								>
									<img src="https://placeimg.com/192/192/people" alt="avatar" />
								</div>
							</div>
							<div class="">
								<h1 class="text-2xl font-bold">ChiefMonkey</h1>
							</div>
						</div>
						<p class="text-xl font-bold">Winner!</p>
					</div>
					<div class="place-items-start grid my-4">
						<h2 class="card-title lg:text-5xl text-left">1 hour one-to-one call with Gigi AMA</h2>
						<!-- <button class="p-1 bg-red-400 text-sm uppercase rounded">Auction ended</button> -->
					</div>
					<p />
					<p class="text-left">
						We will chat through Jitsi face to face although I will be wearing a mask. We can talk
						about anything apart from shitcoins.
					</p>
					<!-- AVATAR -->
					<div class="flex items-center space-x-4 my-4">
						<div class="avatar">
							<div
								class="w-12 h-12 rounded-full ring ring-primary ring-offset-base-100 ring-offset-2"
							>
								<img src="https://placeimg.com/192/192/people" alt="avatar" />
							</div>
						</div>
						<div class="">
							<h1 class="text-2xl font-bold">Gigi</h1>
						</div>
					</div>
					<div class="flex justify-between items-center mt-8">
						<a href="/campaign/auction" class="uppercase font-bold">See Details</a>
						<p class="text-left text-sm font-mono text-gray-500">2022-01-03</p>
					</div>
				</div>
			</div>
		</div>
	</div>
</div>
