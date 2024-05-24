<script lang="ts">
	import Button from '$lib/components/Button.svelte';
	import StarRating from './StarRating.svelte';

	export let title: string;
	export let subtitle: string = '';
	export let imageSrc: string;
	export let star: number;
	export let color: string;
	export let siteName: string;
	export let claimLink: string;
</script>

<card class="rounded-2xl flex flex-col w-[350px] overflow-hidden bg-white shadow-sm items-center">
	<div
		class="text-white font-bold text-center py-1 m-4 rounded-2xl  w-[280px]  h-[280px]
        flex flex-col justify-center items-center relative"
		style="background-color: {color}"
	>
		<img src={imageSrc} alt="{siteName}' logo" class="w-48 h-44 rounded-3xl" />
        <div class=" absolute bottom-8 right-[50%] transform translate-x-[50%]">
			<StarRating {star} />
		</div>
	</div>

	<div class="title-container">
		<div>
			{title}
		</div>
		<p>
            {subtitle}
        </p>
	</div>

	<div class="bonus-title">
		<div class="flex flex-row justify-evenly w-full mt-4">
			<Button text="Claim Bonus" href={claimLink} />
		</div>
	</div>
</card>

<style lang="postcss">
	.bonus-title {
		@apply py-3 flex flex-col justify-center items-center;
	}

	.title {
		@apply text-[#1E84F0] text-center;
	}
	.value {
		@apply text-black text-center font-semibold;
	}

	.vl {
		@apply rounded-md;
		width: 2px;
		background-color: #07a1f4;
	}

    .title-container{
        @apply flex flex-row font-bold text-2xl justify-center items-center relative py-4;
        color: var(--text-accent)
    }
</style>
