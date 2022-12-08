<script lang="ts">
	import { onMount } from 'svelte';
	const endpoint = 'https://api.coinlore.net/api/ticker/?id=90';

	interface BitcoinData {
		id: string;
		price_usd: string;
		percent_change_24h: string;
		rank: number;
	}

	let ticker: BitcoinData[] = [];

	onMount(async function () {
		const res = await fetch(endpoint);
		const data = await res.json();
		ticker = data;
	});
</script>

{#each ticker as data}
	<p>${data.price_usd}</p>
{/each}
