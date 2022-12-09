<script lang="ts">
	let openTab = 1;

	function toggleTabs(tabNumber: number) {
		openTab = tabNumber;
	}
</script>

<div class="flex flex-wrap">
	<div class="w-full">
		<ul class="flex my-4">
			<li class="-mb-px mr-2 last:mr-0 text-center">
				<button
					class="text-xs font-bold uppercase px-5 py-3 shadow-lg rounded block leading-normal {openTab ===
					1
						? 'text-white bg-orange-600'
						: 'text-orange-600 bg-white'}"
					on:click={() => toggleTabs(1)}
					on:keydown={() => {
						toggleTabs;
					}}
				>
					Project Details
				</button>
			</li>
			<li class="-mb-px mr-2 last:mr-0 text-center">
				<button
					class="text-xs font-bold uppercase px-5 py-3 shadow-lg rounded block leading-normal {openTab ===
					2
						? 'text-white bg-orange-600'
						: 'text-orange-600 bg-white'}"
					on:click={() => toggleTabs(2)}
				>
					Tab2
				</button>
			</li>
			<li class="-mb-px mr-2 last:mr-0 flex-auto text-center">
				<button
					class="text-xs font-bold uppercase px-5 py-3 shadow-lg rounded block leading-normal {openTab ===
					3
						? 'text-white bg-orange-600'
						: 'text-orange-600 bg-white'}"
					on:click={() => toggleTabs(3)}
				>
					Tab3
				</button>
			</li>
		</ul>
		<div
			class="relative flex flex-col min-w-0 break-words bg-white dark:bg-gray-900 border border-white/20 w-full mb-6 shadow-lg rounded"
		>
			<div class="px-4 py-5 flex-auto">
				<div class="tab-content tab-space">
					<div class={openTab === 1 ? 'block' : 'hidden'}>
						<p>
							We will chat through Jitsi face to face although I will be wearing a mask. We can talk
							about anything apart from shitcoins.
						</p>
					</div>
					<div class={openTab === 2 ? 'block' : 'hidden'}>
						<p>tab2</p>
					</div>
					<div class={openTab === 3 ? 'block' : 'hidden'}>
						<p>tab3</p>
					</div>
				</div>
			</div>
		</div>
	</div>
</div>
