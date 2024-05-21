<script lang="ts">
	import BitcoinRating from './BitcoinRating.svelte';
	import Button from './Button.svelte';
	import StarRating from './StarRating.svelte';

	export let payoutTime: string = '1-5 days';
	export let winRate: string = '97.5%';
	export let playNowLink: string = '/';
	export let bitcoinStarRage: number = 4;
	export let reviewLink: string = '/';
	export let star: number = 4;
	export let title: string = 'Casino 1';
	export let code: string = 'CODE';
	export let image: string = 'https://via.placeholder.com/150';
	export let valueOfFreeSpins: string = '$200';
	export let details: string[] = [
		'100% up to $500',
		'200 Free Spins For Wacky Panda, Book of Dead'
	];
</script>

<card>
	<div class="header">
		<img src={image} alt={title} />
		<div>
			<div class="py-1">
				<span class="font-bold">
					{title}
				</span>
			</div>

			<StarRating {star} />
		</div>
	</div>

	<div class="border-b-[1px] border-gray-200 px-4 py-2 flex flex-col gap-2">
		{#each details as detail}
			<div class="flex flex-row items-start gap-2">
				<div class="w-[10px] h-[10px]">
					<svg
						class="mt-1"
						xmlns="http://www.w3.org/2000/svg"
						width="10"
						height="13"
						viewBox="0 0 7 8"
						fill="none"
					>
						<path d="M7 4.21319L0.804157 0.636017L0.804157 7.79036L7 4.21319Z" fill="#9D9D9D" />
					</svg>
				</div>
				<span class="text-black font-semibold text-sm detail">
					{detail}
				</span>
			</div>
		{/each}

		<span class="text-black font-light text-sm">
			Value of free spins: {valueOfFreeSpins}
		</span>
	</div>

	<div class="flex flex-row justify-evenly items-center py-4">
		<div class="flex flex-col justify-center items-center">
			<span> Payout time </span>
			<span class="font-light">
				{payoutTime}
			</span>
		</div>

		<div class="flex flex-col justify-center items-center">
			<span> Win Rate </span>
			<span class="font-light">
				{winRate}
			</span>
		</div>

		<div>
			<Button text="Play Now" href={playNowLink} size="lg" />
		</div>
	</div>

	<div class="bitcoin-rate">
		<BitcoinRating rate={bitcoinStarRage} />
	</div>

    {#if !!code }
        <div class="code-container">
            Use Code: {code}
        </div>
    {/if}
</card>

<style lang="scss">
	card {
		@apply flex flex-col;
		@apply bg-white rounded-2xl shadow-lg;
		@apply relative;
		width: 350px;
	}

	.bitcoin-rate {
        background: #F8F8F8;
		position: absolute;
        bottom: -34px;
        right: 0;
        transform: translateX(-50%);
        padding: 10px;
        @apply rounded-b-2xl;
	}

	.header {
		@apply flex flex-row justify-start items-center gap-2;
		@apply p-4;
		img {
			@apply rounded-2xl;
			width: 114px;
			height: 70px;
		}
	}

    .detail{
        width: calc(100% - 20px)
    }

    .code-container{
        @apply  text-white font-extrabold bg-gradient-to-br from-[#6B14CE] to-[#CA1F8E];
        @apply rounded-2xl px-2 py-1 text-center text-sm;
        position: absolute;
        top: 0;
        right: 20px;
        transform: translateY(-50%);
    }
</style>
