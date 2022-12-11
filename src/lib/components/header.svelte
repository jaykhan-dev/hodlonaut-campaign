<script>
	import NewLogo from '$lib/images/new-logo.svg';
	import BitcoinPrice from './bitcoinPrice.svelte';
	import { fade } from 'svelte/transition';
	import { darkTheme } from '../../Store';

	let showMenu = false;

	function toggleNavbar() {
		showMenu = !showMenu;
	}

	const wait = () => new Promise((res) => setTimeout(res, 1000));

	const toggleDark = () => ($darkTheme = !$darkTheme);
	$: dark = $darkTheme;
</script>

<header class="bg-gray-900/80 backdrop-blur-md border-b border-white/20 fixed top-0 w-full z-50">
	<nav class="lg:w-2/3 py-4 px-4 mx-auto md:flex md:justify-between md:items-center">
		<div class="flex items-center justify-between">
			<div class="flex items-center space-x-2">
				<img src={NewLogo} alt="Plebeian Market logo" width={40} />
				<a class="text-xl font-bold md:text-2xl hover:text-blue-400" href="/">Plebeian Market </a>
			</div>
			<!-- Mobile menu button -->
			<div
				on:click={toggleNavbar}
				on:keydown={() => {
					toggleNavbar;
				}}
				class="flex md:hidden"
			>
				<button
					type="button"
					class="text-gray-400 hover:text-gray-600 focus:outline-none focus:text-gray-400"
				>
					<svg
						xmlns="http://www.w3.org/2000/svg"
						fill="none"
						viewBox="0 0 24 24"
						stroke-width="1.5"
						stroke="currentColor"
						class="w-6 h-6"
					>
						<path
							stroke-linecap="round"
							stroke-linejoin="round"
							d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5"
						/>
					</svg>
				</button>
			</div>
		</div>

		<!-- Mobile Menu open: "block", Menu closed: "hidden" -->
		<div
			class="flex-col mt-8 space-y-4 md:flex md:space-y-0 md:flex-row md:items-center md:space-x-4 md:mt-0 {showMenu
				? 'flex'
				: 'hidden'}"
		>
			<div class="flex space-x-4 lg:mx-4">
				<div class="dropdown">
					<button class="flex items-center">Campaign</button>
					<ul class="dropdown-content menu p-2 shadow bg-base-100 rounded-box w-36">
						<li><a href="/campaign/hodlonaut">Hodlonaut</a></li>
						<li><a href="/campaign/auction">Auction</a></li>
					</ul>
				</div>

				<div class="dropdown">
					<button class="">Scenes</button>
					<ul class="dropdown-content menu p-2 shadow bg-base-100 rounded-box w-36">
						<li><a href="/scenes/one">One</a></li>
						<li><a href="/scenes/two">Two</a></li>
						<li><a href="/scenes/three">Three</a></li>
					</ul>
				</div>
			</div>
			{#await wait()}
				<p class="mx-8">loading...</p>
			{:then show}
				<div transition:fade>
					<BitcoinPrice />
				</div>
			{/await}
			<!-- LIGHT MODE AND AVATAR -->
			<div class="flex items-center space-x-4">
				<div>
					<label class="swap swap-rotate">
						<!-- this hidden checkbox controls the state -->
						<input type="checkbox" on:click={toggleDark} />

						<!-- sun icon -->
						<svg
							class="swap-on fill-current w-10 h-10"
							xmlns="http://www.w3.org/2000/svg"
							viewBox="0 0 24 24"
							><path
								d="M5.64,17l-.71.71a1,1,0,0,0,0,1.41,1,1,0,0,0,1.41,0l.71-.71A1,1,0,0,0,5.64,17ZM5,12a1,1,0,0,0-1-1H3a1,1,0,0,0,0,2H4A1,1,0,0,0,5,12Zm7-7a1,1,0,0,0,1-1V3a1,1,0,0,0-2,0V4A1,1,0,0,0,12,5ZM5.64,7.05a1,1,0,0,0,.7.29,1,1,0,0,0,.71-.29,1,1,0,0,0,0-1.41l-.71-.71A1,1,0,0,0,4.93,6.34Zm12,.29a1,1,0,0,0,.7-.29l.71-.71a1,1,0,1,0-1.41-1.41L17,5.64a1,1,0,0,0,0,1.41A1,1,0,0,0,17.66,7.34ZM21,11H20a1,1,0,0,0,0,2h1a1,1,0,0,0,0-2Zm-9,8a1,1,0,0,0-1,1v1a1,1,0,0,0,2,0V20A1,1,0,0,0,12,19ZM18.36,17A1,1,0,0,0,17,18.36l.71.71a1,1,0,0,0,1.41,0,1,1,0,0,0,0-1.41ZM12,6.5A5.5,5.5,0,1,0,17.5,12,5.51,5.51,0,0,0,12,6.5Zm0,9A3.5,3.5,0,1,1,15.5,12,3.5,3.5,0,0,1,12,15.5Z"
							/></svg
						>

						<!-- moon icon -->
						<svg
							class="swap-off fill-current w-10 h-10"
							xmlns="http://www.w3.org/2000/svg"
							viewBox="0 0 24 24"
							><path
								d="M21.64,13a1,1,0,0,0-1.05-.14,8.05,8.05,0,0,1-3.37.73A8.15,8.15,0,0,1,9.08,5.49a8.59,8.59,0,0,1,.25-2A1,1,0,0,0,8,2.36,10.14,10.14,0,1,0,22,14.05,1,1,0,0,0,21.64,13Zm-9.5,6.69A8.14,8.14,0,0,1,7.08,5.22v.27A10.15,10.15,0,0,0,17.22,15.63a9.79,9.79,0,0,0,2.1-.22A8.11,8.11,0,0,1,12.14,19.73Z"
							/></svg
						>
					</label>
				</div>
				<!-- AVATAR -->
				<div class="avatar">
					<div class="w-8 rounded-full ring ring-primary ring-offset-base-100 ring-offset-2">
						<img src="https://placeimg.com/192/192/people" alt="avatar" />
					</div>
				</div>
			</div>
		</div>
	</nav>
</header>
