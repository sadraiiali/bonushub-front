<script lang="ts">
	import type { HeaderItem } from '$lib/types';

	export let items: HeaderItem[] = [
		{ name: 'Gambling Guide', path: '/gambling-guide' },
		{ name: 'News', path: '/news' },
		{ name: 'Bitcoin Casinos', path: '/bitcoin-casinos' },
		{ name: 'About Us', path: '/about-us' },
		{ name: 'Contact', path: '/contact' }
	];
	export let title: string = 'BonusHub';
</script>

<header>
	<div class="header-container">
		<h1 class="title-text-gradient">
			<a href="/">
				{title}
			</a>
		</h1>
		<nav>
			<ul>
				{#each items as item}
					<li>
						<a href={item.path}>
							{item.name}
						</a>
					</li>
				{/each}
			</ul>
		</nav>
	</div>
</header>

<style lang="postcss">
	header {
		@apply bg-white text-black p-4;
		min-height: var(--header-height);
	}

	.header-container {
		@apply container mx-auto h-full;
		@apply flex flex-col sm:flex-row justify-between items-center;
	}

	ul {
		@apply flex flex-row flex-wrap justify-center sm:justify-end space-x-4;
	}

	li {
		@apply list-none w-32 h-10 text-left flex justify-center sm:justify-center items-center;
		color: var(--text-color-2);
	
	}
	h1 {
		@apply text-5xl py-8 sm:p-0 sm:text-2xl font-extrabold;
	}
</style>
