<script lang="ts">
	import Button from '$lib/components/Button.svelte';
	import StarRating from './StarRating.svelte';

	export let title: string;
	export let imageSrc: string;
	export let star: number;
	export let playNowLink: string;
	export let reviewLink: string;
	export let payout: string;
	export let winRate: string;
	export let bonus: string;
	export let color: string;
	export let siteName: string;
</script>

<card class="rounded-3xl flex flex-col w-[350px] overflow-hidden bg-white shadow-md">
	<div class="text-white font-bold text-center py-1" style="background-color: {color}">
		{title}
	</div>

	<div class="flex flex-row justify-center items-center relative py-4">
		<img src={imageSrc} alt="{siteName}' logo" class="w-48 h-44 rounded-3xl" />

		<div class=" absolute bottom-8 right-[50%] transform translate-x-[50%]">
            <StarRating star={star} />  
        </div>
	</div>

	<div class="bonus-title">
		<h4 class="text-black font-bold">Bonus</h4>

		<h5 class="text-[#07A1F4] font-bold">
			{bonus}
		</h5>

		<div class="flex flex-row justify-evenly w-full mt-4">
			<Button text="Play Now" href="/" />
			<Button text="Review" type="OUTLINE" href="/" />
		</div>
	</div>

    <div class="py-4 flex flex-row justify-evenly">
        <div class="flex flex-col">
            <span class="title">
                Payout 🕑
            </span>
            <span class="value">
                {payout}
            </span>
        </div>
        
        <div class="vl">
            &nbsp;	
        </div>

        <div class="flex flex-col">
            <span class="title">
                Win rate
            </span>
            <span class="value">
                {winRate}
            </span>
        </div>
    </div>
</card>

<style lang="postcss">

	.bonus-title {
		@apply py-3 flex flex-col justify-center items-center;
		background: rgba(120, 209, 255, 0.23);
	}

    .title{
        @apply text-[#1E84F0] text-center;
    }
    .value{
        @apply text-black text-center font-semibold;
    }

    .vl{
        @apply rounded-md;
        width: 2px;
        background-color: #07A1F4;
    
        
    }
</style>
