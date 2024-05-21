<script lang="ts">
	export let title: string;
	export let description: string;
	export let imgSrc: string;
</script>

<card>
	<div class="bg"
     style="background-image: url({imgSrc}); background-size: cover; background-position: center;">

    </div>
	<h3 class="">
		{title}
	</h3>
	<p>
		{description}
	</p>
</card>

<style lang="scss">
	card {
		height: 400px;
		width: 300px;
		@apply flex flex-col justify-start gap-3;
        @apply rounded-2xl bg-white overflow-hidden relative;
        .bg{
            @apply bg-[#F8F8F8] w-full ;
            height: 200px;
        }
		h3 {
			color: #027b5b;
            @apply text-center font-bold text-2xl;
		}

		p {
			@apply text-black text-justify text-sm;
            @apply px-8;

		}
	}
</style>
