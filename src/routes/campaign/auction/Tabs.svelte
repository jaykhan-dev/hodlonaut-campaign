<script lang="ts">
	let openTab = 1;

	function toggleTabs(tabNumber: number) {
		openTab = tabNumber;
	}
</script>

<div class="flex flex-wrap lg:w-2/3 mx-auto p-2">
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
					Profile
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
					Settings
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
					Options
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
							Collaboratively administrate empowered markets via plug-and-play networks. Dynamically
							procrastinate B2C users after installed base benefits.
							<br />
							<br />
							Dramatically visualize customer directed convergence without revolutionary ROI.
						</p>
					</div>
					<div class={openTab === 2 ? 'block' : 'hidden'}>
						<p>
							Completely synergize resource taxing relationships via premier niche markets.
							Professionally cultivate one-to-one customer service with robust ideas.
							<br />
							<br />
							Dynamically innovate resource-leveling customer service for state of the art customer service.
						</p>
					</div>
					<div class={openTab === 3 ? 'block' : 'hidden'}>
						<p>
							Efficiently unleash cross-media information without cross-media value. Quickly
							maximize timely deliverables for real-time schemas.
							<br />
							<br />
							Dramatically maintain clicks-and-mortar solutions without functional solutions.
						</p>
					</div>
				</div>
			</div>
		</div>
	</div>
</div>
