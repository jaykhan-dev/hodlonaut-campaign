<script>
	import Tabs from './Tabs.svelte';
	import SpaceCat from '$lib/images/space-cat.png';
</script>

<div class="p-4 grid place-items-center bg-white dark:bg-gray-900 text-black dark:text-white">
	<div class="grid place-items-center lg:w-2/3 mx-auto pt-20">
		<div class="w-full">
			<p class="text-center py-4 bg-red-300 text-black">Auction ended</p>
			<h1 class="lg:text-7xl text-3xl font-black my-8">1 hour one-to-one call with Gigi AMA</h1>
			<div class="grid lg:grid-cols-2 gap-4 border-t border-white/20 pt-8">
				<!-- COL -->
				<div class="">
					<img src={SpaceCat} class="w-full" alt="" />
				</div>
				<!-- COL -->
				<div>
					<div class="flex space-x-4 mb-8">
						<div class="avatar">
							<div
								class="w-12 h-12 rounded-full ring ring-primary ring-offset-base-100 ring-offset-2"
							>
								<img src="https://placeimg.com/192/192/people" alt="avatar" />
							</div>
						</div>
						<div class="">
							<h1 class="text-4xl font-bold">Gigi</h1>
						</div>
					</div>
					<div class="flex space-x-4 py-4">
						<button class="text-sm p-1 font-mono border rounded border-white/20 uppercase"
							>We Are All Hodlonaut Campaign</button
						>
					</div>
					<Tabs />
				</div>
			</div>
		</div>
	</div>
</div>

<div class="text-black dark:text-white grid place-items-center bg-white dark:bg-gray-900 pb-20 p-4">
	<div class="lg:w-2/3 mx-auto">
		<h1 class="text-6xl font-bold my-8">Bids</h1>
		<!-- ROW -->
		<div
			class="text-white grid grid-cols-4 gap-4 border p-4 bg-gray-800 rounded border-white/20 my-2 font-bold uppercase"
		>
			<!-- COL -->
			<div class="col-span-2">
				<h1>Bidder</h1>
			</div>
			<!-- COL -->
			<div>
				<h1>Amount</h1>
			</div>
			<!-- COL -->
			<div>
				<h1>Date</h1>
			</div>
		</div>

		<!-- ROW -->
		<div class="grid grid-cols-4 gap-4 border-b p-4 border-white/20 my-2">
			<!-- COL -->
			<div class="col-span-2 flex items-center space-x-4">
				<div class="avatar">
					<div class="w-8 rounded-full ring ring-primary ring-offset-base-100 ring-offset-2">
						<img src="https://placeimg.com/192/192/people" alt="avatar" />
					</div>
				</div>
				<h1>ChiefMonkey</h1>
			</div>
			<!-- COL -->
			<div>
				<h1>11 sats ($0.00)</h1>
			</div>
			<!-- COL -->
			<div>
				<h1>Nov 14 7:23</h1>
			</div>
		</div>

		<!-- ROW -->
		<div class="grid grid-cols-4 gap-4 border-b p-4 border-white/20 my-2">
			<!-- COL -->
			<div class="col-span-2 flex items-center space-x-4">
				<div class="avatar">
					<div class="w-8 rounded-full ring ring-primary ring-offset-base-100 ring-offset-2">
						<img src="https://placeimg.com/192/192/people" alt="avatar" />
					</div>
				</div>
				<h1>ChiefMonkey</h1>
			</div>
			<!-- COL -->
			<div>
				<h1>10 sats ($0.00)</h1>
			</div>
			<!-- COL -->
			<div>
				<h1>Nov 14 7:21</h1>
			</div>
		</div>
	</div>
</div>
