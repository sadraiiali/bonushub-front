<script lang="ts">
	export let rate: number = 0;
</script>

<div class="flex flex-row justify-center items-center gap-1">
	{#each Array(rate) as _}
		<img src="/img/bitcoin-icon.png" alt="Bitcoin Icon" class="w-4 h-4" />
	{/each}

	{#each Array(4 - rate) as _}
		<img src="/img/bitcoin-icon.png" alt="Bitcoin Icon" class="w-4 h-4 opacity-20" />
	{/each}
</div>
