<script lang="ts">
	import Button from "./Button.svelte";

    export let imgSrc: string;
    export let title: string;
    export let href: string;
</script>



<card>
    <img src={imgSrc} alt="{title}'s Logo" class="w-40 h-40 rounded-full" />
    <h3>
        {title}
    </h3>

    <Button text="select" />
</card>


<style lang="scss">
    card{
        background: white;
        @apply p-4 rounded-2xl shadow-md;
        @apply flex flex-col justify-center items-center gap-3;
        h3{
            @apply text-[#0368EE] text-xl font-bold;
        }
    }
</style>