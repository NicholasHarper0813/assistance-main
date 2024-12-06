<script lang="ts">
	// Components
	import Marquee from 'svelte-fast-marquee';

	// Icons
	import Solana from './icons/solana.svelte';
	import Logo from './icons/logo.svelte';

	import { onMount } from 'svelte';

	const TAB_WIDTH = 768;

	let windowWidth = 0;

	onMount(() => {
		windowWidth = window.innerWidth;
		window.addEventListener('resize', () => {
			windowWidth = window.innerWidth;
		});

		return () => {
			window.removeEventListener('resize', () => {
				windowWidth = window.innerWidth;
			});
		};
	});
</script>

<div>
	<Marquee>
		{#each Array(20) as _, index}
			<div class="flex h-20 items-center gap-3">
				<span class="whitespace-nowrap pt-1 font-semibold leading-none">SOLANA HACKATHON</span>
				<Logo className="h-4" />
			</div>
		{/each}
	</Marquee>
</div>

<div class="container-custom mx-auto mb-[200px]">
	<h2 class="font-victor py-16 text-center text-4xl font-medium italic md:text-[56px]">
		With Support From
	</h2>
	<div class="grid grid-cols-2 gap-4 sm:grid-cols-3 md:grid-cols-4 lg:grid-cols-5">
		{#each Array(windowWidth < TAB_WIDTH ? 12 : 20) as _, index}
			<div class="border bg-[#F6F6F6] p-[2px]">
				<div
					class="text-dark1 hover:bg-dark1 flex h-[100px] cursor-pointer items-center justify-center border bg-white duration-300 hover:text-white"
				>
					<Solana />
				</div>
			</div>
		{/each}
	</div>
</div>
