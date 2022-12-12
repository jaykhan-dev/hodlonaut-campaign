<script lang="ts">
	import Auctions from './Auctions.svelte';

	let openTab = 2;

	function toggleTabs(tabNumber: number) {
		openTab = tabNumber;
	}
</script>

<div class="flex flex-wrap p-2 bg-white dark:bg-gray-900">
	<div class="w-full lg:w-2/3 mx-auto">
		<ul class="tabs flex my-4 justify-center">
			<li class="-mb-px mr-2 last:mr-0 text-center">
				<button
					class="text-xs font-bold uppercase px-5 py-3 block tab border-b leading-normal {openTab ===
					1
						? 'tab-active border-b-4'
						: 'tab'}"
					on:click={() => toggleTabs(1)}
					on:keydown={() => {
						toggleTabs;
					}}
				>
					Active
				</button>
			</li>
			<li class="-mb-px mr-2 last:mr-0 text-center">
				<button
					class="text-xs font-bold uppercase px-5 py-3 block tab border-b leading-normal {openTab ===
					2
						? 'tab-active border-b-4'
						: 'tab'}"
					on:click={() => toggleTabs(2)}
				>
					Past
				</button>
			</li>
		</ul>
		<div class="relative flex flex-col min-w-0 break-words bg-white dark:bg-gray-900 w-full mb-6">
			<div class="px-4 py-5 flex-auto">
				<div class="tab-content tab-space">
					<div class={openTab === 1 ? 'block' : 'hidden'} />
					<div class={openTab === 2 ? 'block' : 'hidden'}>
						<Auctions />
					</div>
				</div>
			</div>
		</div>
	</div>
</div>
