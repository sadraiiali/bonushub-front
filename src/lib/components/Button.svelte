<script lang="ts">
    export let text: string;
    export let href: string;
    export let action: () => void;
    export let type: "NORMAL" | "TYPE2" | "OUTLINE" = "NORMAL";
    export let size: "sm" | "md" | "lg" = "md";
    export let color: "PRIMARY" | "SECONDARY" | "TERTIARY";
</script>

{#if type==="NORMAL"}
    <a
        class="rounded-3xl py-2 px-4 min-w-32 text-md text-center shadow-lg font-bold flex flex-row justify-center items-center text-white bg-[#07A1F4]"
        href={href}
    >
        {text}
    </a>

{:else if type==="OUTLINE"}
    <a
        class="rounded-3xl py-2 px-4 min-w-32 text-md text-center shadow-lg font-bold flex flex-row justify-center items-center text-[#07A1F4] border-2 border-[#07A1F4] bg-white"
        href={href}
    >
    {text}
    </a>

{:else if type==="TYPE2"}
    <a
        class="rounded-3xl py-2 px-4 min-w-32 text-md text-center font-bold flex flex-row justify-center items-center text-[#07A1F4] border-2 border-[#07A1F4] bg-transparent"
        href={href}
    >
    {text}
    </a>
{/if}


<style>

</style>
