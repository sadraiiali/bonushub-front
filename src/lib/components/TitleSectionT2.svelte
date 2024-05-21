<script lang="ts">
	export let title: string;
	export let subtitle: string;
	export let subtitle2: string;
</script>

<div class="text-center my-4 flex flex-col gap-3">
	<h2 class="title-text-gradient-2 text-2xl font-extrabold">
		{title}
	</h2>
	<p class="text-[#0580F1] text-4xl font-light">
		{subtitle}
	</p>

	{#if subtitle2}
        <p class="font-xs text-[#5E5E5E]">
            {subtitle2}
        </p>
    {/if}
</div>
