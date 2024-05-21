<script>
	let bonusesLinks = [
		{
			name: 'Casino Bonuses',
			link: '/casino-bonuses'
		},
		{
			name: 'Free Spins No Deposit',
			link: '/free-spins-no-deposit'
		},
		{
			name: 'Best Online Casinos',
			link: '/best-online-casinos'
		},
		{
			name: 'New Casinos 2024',
			link: '/new-casinos'
		},
		{
			name: 'Bitcoin Casinos',
			link: '/bitcoin-casinos'
		},
		{
			name: 'Guides',
			link: '/guides'
		},
		{
			name: 'News',
			link: '/news'
		},
		{
			name: 'All Bonuses',
			link: '/all-bonuses'
		}
	];

	let companiesLink = [
		{
			name: 'Privacy Policy',
			link: '/privacy-policy'
		},
		{
			name: 'Responsable Gambling',
			link: '/responsible-gambling'
		},
		{
			name: 'About Us',
			link: '/about-us'
		},
		{
			name: 'How we Review',
			link: '/how-we-review'
		},
		{
			name: 'Contact Us',
			link: '/contact-us'
		}
	];
</script>

<footer>
	<div class="container m-auto ">
		<div class="flex flex-row justify-between py-16">
			
            <h2 class="text-6xl text-white font-extrabold px-4 ">
                BonusHub
            </h2>
			<div class="flex flex-row gap-4">
				<div class="flex flex-col gap-4">
                    <h3 class="text-white font-bold text-2xl">
                        Bonuses
                    </h3>
					{#each bonusesLinks as bonusLink}
						<a href={bonusLink.link} class="text-gray-200 text-2xl font-light hover:text-blue-500">{bonusLink.name}</a>
					{/each}
				</div>

				<div class="flex flex-col gap-4">
                    <h3 class="text-white font-bold text-2xl">
                        Company
                    </h3>
					{#each companiesLink as companyLink}
						<a href={companyLink.link} class="text-gray-200 text-2xl font-light hover:text-blue-500">{companyLink.name}</a>
					{/each}
				</div>
			</div>
		</div>
	</div>
</footer>

<style lang="postcss">
	footer {
		min-height: 500px;
		@apply bg-gradient-to-br from-[#09C6F8] to-[#0263ED];
	}
</style>
