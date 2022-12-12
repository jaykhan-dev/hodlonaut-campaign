<script>
	import SceneOne from '$lib/images/3d_satoshi.png';
	import SceneTwo from '$lib/images/3d_iphone.png';
	import SceneThree from '$lib/images/3d_cube.png';
</script>

<div class="min-h-screen grid place-items-center">
	<div class="lg:w-2/3 mx-auto grid lg:grid-cols-3 gap-8 my-20 py-20 p-4">
		<!-- COL -->
		<div>
			<a href="/scenes/one" class="">
				<img
					src={SceneOne}
					alt="Spine scene 1"
					class="opacity-80 hover:opacity-100 duration-300 hover:scale-95"
				/>
				<p class="uppercase text-sm my-4">Scene One made with Spline</p>
			</a>
		</div>

		<!-- COL -->
		<div>
			<a href="/scenes/two">
				<img
					src={SceneTwo}
					alt="Spline scene 2"
					class="opacity-80 hover:opacity-100 duration-300 hover:scale-95"
				/>
				<p class="uppercase text-sm my-4">Scene Two made with Spline</p>
			</a>
		</div>

		<!-- COL -->
		<div>
			<a href="/scenes/three">
				<img
					src={SceneThree}
					alt="Svelte-cubed scene"
					class="opacity-80 hover:opacity-100 duration-300 hover:scale-95"
				/>
				<p class="uppercase text-sm my-4">Scene Three made with Svelte-cubed</p>
			</a>
		</div>
	</div>
</div>
