<script>
	import Header from '$lib/components/layouts/Header.svelte';
	import Banner2 from '$lib/components/Banner2.svelte';
	import TitleSection from '$lib/components/TitleSection.svelte';
	import CasinoChoiceCard2 from '$lib/components/CasinoChoiceCard2.svelte';
	import SubTitleSection from '$lib/components/SubTitleSection.svelte';
	import Button from '$lib/components/Button.svelte';
	import CasinoReviewSmallCard from '$lib/components/CasinoReviewSmallCard.svelte';
	import TitleSectionT2 from '$lib/components/TitleSectionT2.svelte';
	import CasinosListMini from '$lib/components/CasinosListMini.svelte';
	import NewsCard from '$lib/components/NewsCard.svelte';
	import Footer from '$lib/components/layouts/Footer.svelte';

	let casinoChoices = [
		{
			title: 'Casino 1',
			imageSrc: '/logos/spin_casino_logo.svg',
			star: 4,
			color: '#CC99FF',
			siteName: 'Casino 1',
			playNowLink: '/',
			reviewLink: '/',
			payout: '98%',
			winRate: '98%',
			bonus: '100% up to $1,000 + 200 Free Spins'
		},
		{
			title: 'Casino 1',
			imageSrc: 'https://via.placeholder.com/150',
			star: 4,
			color: '#FF9900',
			siteName: 'Casino 1',
			playNowLink: '/',
			reviewLink: '/',
			payout: '98%',
			winRate: '98%',
			bonus: '100% up to $1,000 + 200 Free Spins'
		},
		{
			title: 'Casino 1',
			imageSrc: 'https://via.placeholder.com/150',
			star: 4,
			color: '#00D709',
			siteName: 'Casino 1',
			playNowLink: '/',
			reviewLink: '/',
			payout: '98%',
			winRate: '98%',
			bonus: '100% up to $1,000 + 200 Free Spins'
		}
	];

	let casinoReviews = [
		{
			title: 'Casino 1',
			image: 'https://via.placeholder.com/150',
			star: 4,
			details: ['100% up to $500', '200 Free Spins For Wacky Panda, Book of Dead'],
			valueOfFreeSpins: '$200',
			code: 'CODE',
			reviewLink: '/',
			bitcoinStarRage: 4,
			playNowLink: '/',
			winRate: '97.5%',
			payoutTime: '1-5 days'
		},
		{
			title: 'Casino 1',
			image: 'https://via.placeholder.com/150',
			star: 4,
			details: ['100% up to $500', '200 Free Spins For Wacky Panda, Book of Dead'],
			valueOfFreeSpins: '$200',
			code: 'CODE',
			reviewLink: '/',
			bitcoinStarRage: 4,
			playNowLink: '/',
			winRate: '97.5%',
			payoutTime: '1-5 days'
		},
		{
			title: 'Casino 1',
			image: 'https://via.placeholder.com/150',
			star: 4,
			details: ['100% up to $500', '200 Free Spins For Wacky Panda, Book of Dead'],
			valueOfFreeSpins: '$200',
			code: 'CODE',
			reviewLink: '/',
			bitcoinStarRage: 4,
			playNowLink: '/',
			winRate: '97.5%',
			payoutTime: '1-5 days'
		}
	];

	let categories = [
		{
			imgSrc: '/img/baccarat_cat_icon.png',
			title: 'Baccarat',
			href: '/baccarat'
		},
		{
			imgSrc: '/img/bingo_cat_icon.png',
			title: 'Bingo',
			href: '/bingo'
		},
		{
			imgSrc: '/img/crabs_cat_icon.png',
			title: 'Crabs',
			href: '/crabs'
		},
		{
			imgSrc: '/img/poker_cat_icon.png',
			title: 'Poker',
			href: '/poker'
		},
		{
			imgSrc: '/img/roulette_cat_icon.png',
			title: 'Roulette',
			href: '/roulette'
		},
		{
			imgSrc: '/img/sic_bo_cat_icon.png',
			title: 'Sic Bo',
			href: '/sic-bo'
		},
		{
			imgSrc: '/img/slots_cat_icon.png',
			title: 'Slots',
			href: '/slots'
		},
		{
			imgSrc: '/img/blackjack_cat_icon.png',
			title: 'Blackjack',
			href: '/blackjack'
		}
	];


	let news = [
		{
			title: 'Title',
			description: 'Explore our selection of exclusive & up to date bonuses, boosting your bankroll and giving you a bang for your buck everytime.',
			imgSrc: 'https://via.placeholder.com/150'
		},
		{
			title: 'Title',
			description: 'Explore our selection of exclusive & up to date bonuses, boosting your bankroll and giving you a bang for your buck everytime.',
			imgSrc: 'https://via.placeholder.com/150'
		},
		{
			title: 'Title',
			description: 'Explore our selection of exclusive & up to date bonuses, boosting your bankroll and giving you a bang for your buck everytime.',
			imgSrc: 'https://via.placeholder.com/150'
		},
	]
</script>

<div class="flex flex-col">
	<Header />
	<div class="content-container">
		<content class="pt-9">
			<Banner2 />

			<div class="my-16" />
			<div class="w-full max-w-[1120px] m-auto">
				<TitleSection
					title="The #1 Hub for casino and sportsbook reviews"
					subtitle="Our team of seasoned gambling experts has successfully paired thousands of users with their ideal online casino"
				/>

				<div class="flex flex-col justify-center items-center gap-8">
					<div class="flex flex-row gap-8 flex-wrap justify-center items-center">
						{#each casinoChoices as casinoChoice}
							<CasinoChoiceCard2 {...casinoChoice} />
						{/each}
					</div>
					<Button text="View More" type="TYPE2" href="/" />
				</div>
				<div class="my-16" />

				<SubTitleSection title="Best Casinos" />
				<div class="my-16" />
				<div class="flex flex-col justify-center items-center gap-8">
					<div class="flex flex-row gap-8 flex-wrap justify-center items-center mb-10">
						{#each casinoReviews as casinoReview}
							<CasinoReviewSmallCard {...casinoReview} />
						{/each}
					</div>
					<Button text="View More" type="TYPE2" href="/" />
				</div>

				<SubTitleSection title="Best Sports Book" />
				<div class="my-16" />
				<div class="flex flex-col justify-center items-center gap-8">
					<div class="flex flex-row gap-8 flex-wrap justify-center items-center mb-10">
						{#each casinoReviews as casinoReview}
							<CasinoReviewSmallCard {...casinoReview} />
						{/each}
					</div>
					<Button text="View More" type="TYPE2" href="/" />
				</div>

				<div class="mt-32" />
				<TitleSectionT2
					title="Helping gamblers make better choices"
					subtitle="Select one of the following options"
				/>

				<div class="mt-32" />
				<TitleSectionT2
					title="Casino Matchmaker Tool"
					subtitle="What is your game of choice?"
					subtitle2="Select one of the following options"
				/>

				<div class="flex flex-row gap-16 flex-wrap justify-center items-center mb-10">
					{#each categories as category}
						<CasinosListMini {...category} />
					{/each}
				</div>

				<div class="mt-32" />
				<TitleSectionT2
					title="Gambling News"
					subtitle="Check the latest news casino"
				/>
				<div class="flex flex-row gap-8 flex-wrap justify-center items-center mb-10 mt-16">
					{#each news as item}
						<NewsCard {...item} />
					{/each}

				</div>
			</div>


			
		</content>
	</div>

	<Footer />
</div>

<style lang="postcss">
	.content-container {
		@apply flex flex-col;
		background-color: var(--main-bg);

		min-height: calc(100vh - var(--header-height));
		width: 100%;
	}
	content {
		@apply container mx-auto;
	}
</style>
