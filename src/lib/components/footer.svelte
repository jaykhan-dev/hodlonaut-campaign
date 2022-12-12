<script lang="ts">
	import Logo from '$lib/images/pleb-logo-white.svg';
	import Substack from '$lib/images/substack.svg';
</script>

<svelte:head>
	<link
		rel="stylesheet"
		href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.2.1/css/all.min.css"
		integrity="sha512-MV7K8+y+gLIBoVD59lQIYicR65iaqukzvf/nwasF0nqhPay5w/9lJmVM2hMDcnK1OnMGCdVK+iQrJ7lzPJQd1w=="
		crossorigin="anonymous"
		referrerpolicy="no-referrer"
	/>
</svelte:head>

<footer class="text-white lg:p-0 p-4 bg-gray-900 dark:bg-gray-900 border-t border-white/20">
	<!-- SIGNUP -->

	<div class="lg:flex items-center justify-between lg:w-2/3 mx-auto">
		<div>
			<h1 class="lg:text-4xl text-3xl font-bold">Get regular updates</h1>
			<div class="lg:flex lg:space-x-4 my-6">
				<p>&#10003; Weekly</p>
				<p>&#10003; New Releases</p>
				<p>&#10003; New Deals</p>
			</div>
		</div>
		<div class="lg:flex items-center lg:space-x-4 space-y-2">
			<div>
				<button class="btn border-2 border-white flex items-center space-x-2"
					><img src={Substack} width={20} alt="" class="mx-2" /> Substack &#8702;</button
				>
			</div>
			<!-- <button class="btn border-2 border-white">Contact team &#8702;</button> -->
		</div>
	</div>

	<!-- DISCLAIMERS -->
	<div class="border-t border-white/20 lg:w-2/3 mx-auto">
		<div class="lg:flex items-center justify-between py-6">
			<div class="flex items-center space-x-4">
				<p class="">Powered by</p>
				<a href="https://plebian.technology" class="btn">Plebian Technology</a>
			</div>
			<div class="text-2xl flex items-center space-x-4 lg:my-0 my-4 text-white">
				<i class="fa-brands fa-twitter" />
				<i class="fa-brands fa-telegram" />
				<i class="fa-brands fa-github" />
			</div>
		</div>
	</div>
</footer>

<style>
	footer {
		padding-top: 20px;
	}
</style>
