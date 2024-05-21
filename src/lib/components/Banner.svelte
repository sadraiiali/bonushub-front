<script lang="ts">
	import type { CategoryMiniItemCard } from '$lib/types';
	export let title = 'Find the perfect gambling site';
	export let subtitle =
		'BonusHub helps it’s thousands of visitors win big – explore quality bonuses, in-depth reviews, guides and resources';

	export let categories: CategoryMiniItemCard[] = [
		{
			title: 'Best Casinos',
			image: '/img/gold_icon.png',
			url: '/best-casinos'
		},
		{
			title: 'No deposit bonuses',
			image: '/img/bag_of_gold_icon.png',
			url: '/no-deposit-bonuses'
		},
		{
			title: 'Casino reviews',
			image: '/img/casino_role_icon.png',
			url: '/casino-reviews'
		},
		{
			title: 'Free spins',
			image: '/img/reciept_icon.png',
			url: '/free-spins'
		}
	];
</script>

<div class="banner-container">
	<div class="bg-image"></div>
	<div class="content">
		<h1>
			{title}
		</h1>

		<p class="subtitle-text font-bold mb-5">
			{subtitle}
		</p>

		<div class="flex flex-row justify-center items-center gap-5">
			{#each categories as category}
				<a href={category.url}>
					<div
						class="flex flex-col justify-center items-center min-w-40 px-4 py-3 bg-white rounded-3xl shadow-xl
					hover:shadow-2xl transition duration-300 ease-in-out relative hover:scale-105"
					>
						<img src={category.image} alt={category.title} class="shadow-inner rounded-full mb-2" />
						<h2 class="title-text text-center text-blue-600 font-extrabold">
							{category.title}
						</h2>
					</div>
				</a>
			{/each}
		</div>
	</div>
</div>

<style>
	.content {
		@apply h-full w-full flex flex-col justify-center items-center relative;
		@apply gap-4;
		z-index: 2;
	}

	h1 {
		@apply text-5xl font-bold;
	}

	.banner-container {
		background: linear-gradient(180deg, #005bdc 0%, #4e95ff 100%);
		@apply text-white;
		@apply flex flex-col justify-center items-center;
		@apply rounded-3xl relative;
		height: 300px;
	}

	.bg-image {
		@apply bg-cover bg-center h-full w-full absolute rounded-3xl left-0 top-0;
		background-image: url('/img/banner-bg.png');
		opacity: 0.35;
		z-index: 1;
	}

	.title-text-gradient {
		@apply text-4xl font-extrabold;
	}

	.subtitle-text {
		@apply text-lg;
	}
</style>
