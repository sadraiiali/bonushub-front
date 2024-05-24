<script lang="ts">
	import type { CategoryMiniItemCard } from '$lib/types';
	export let title = 'Find the Best Gambling';
	export let subtitle1 = 'Bonuses and Deals';
	export let subtitle2 =
		'BonusFind.ca helps millions of players find the best casinos & sportsbooks - Reviews, Bonuses...';
</script>

<div class="banner-container">
	<div class="content">
		<h1 class="font-extrabold text-5xl">
			{title}
		</h1>

		<p class="subtitle-text font-bold mb-5">
			{subtitle1}
		</p>

		<div class="flex flex-row justify-center items-center gap-5">
			{subtitle2}
		</div>
	</div>
	<div class="bg-image"></div>

</div>

<style lang="postcss">
	.content {
		@apply h-full w-full sm:w-[50%] flex flex-col justify-center items-start relative;
		@apply gap-4 text-center sm:text-left;
		z-index: 2;
	}

	h1 {
		@apply text-4xl sm:text-5xl font-bold;
	}

	.banner-container {
		background: linear-gradient(180deg, #005bdc 0%, #4e95ff 100%);
		@apply text-white;
		@apply flex flex-col justify-center items-start sm:pl-32;
		@apply rounded sm:rounded-3xl relative;
		height: 400px;
	}

	.bg-image {
		@apply bg-cover bg-center h-full w-full absolute rounded-3xl top-0 h-[400px] w-[400px] sm:h-[400px] sm:w-[800px];
		background-image: url('/img/casino-background-logo.png');
		opacity: 0.7;
		z-index: 1;
		right: 0;
	}

	.title-text-gradient {
		@apply text-2xl sm:text-4xl font-extrabold;
	}

	.subtitle-text {
		@apply  text-5xl;
		font-weight: normal;
	}
</style>
