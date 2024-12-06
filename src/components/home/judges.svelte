<script>
	import Judge from '$lib/images/judge.png';
	import JudgeClouds from '$lib/images/judges-clouds.png';
	import Cracks from '$lib/images/cracks.png';

	import { onMount } from 'svelte';
	import Title from '../ui/title.svelte';
	let isMobile = false;

	function checkIsMobile() {
		isMobile = window.innerWidth < 768;
	}

	onMount(() => {
		checkIsMobile();
		window.addEventListener('resize', checkIsMobile);
		return () => {
			window.removeEventListener('resize', checkIsMobile);
		};
	});
</script>

<section class="relative py-24">
	<div class="container-custom relative z-10 mx-auto">
		<div class="mb-20 flex">
			<Title>
				<span class="bg-primary">Judges</span>
			</Title>
		</div>
		<div class="grid grid-cols-2 border-b border-r sm:grid-cols-3 md:grid-cols-4 lg:grid-cols-5">
			{#each Array(Math.min(!isMobile ? 15 : 8, 15)) as _, index}
				<div class="group border-l border-t p-4 xl:px-12 xl:py-8">
					<div>
						<img src={Judge} alt="" class="group-hover:mix-blend-darken" />
						<div>
							<h3 class="font-victor font-medium xl:text-lg">
								<span class="group-hover:bg-primary inline-block duration-300">
									Anatoly Yakovenko
								</span>
							</h3>
							<p class="text-sm font-semibold">Co-founder, Solana Labs</p>
						</div>
					</div>
				</div>
			{/each}
		</div>
		<div class="mt-10 border bg-[#F6F6F6] md:hidden" style="top: calc(100% + 8px)">
			<div class="m-[2px] flex flex-col border bg-white font-medium">
				<button class="w-full py-3 text-center">Load More</button>
			</div>
		</div>
	</div>

	<div
		class="absolute bottom-0 left-0 right-0 top-0 opacity-30"
		style="background: linear-gradient(180deg, #FEFCF9 0%, rgba(254, 252, 249, 0.00) 51%, #FEFCF9 100%), url({JudgeClouds}), lightgray 50% / cover no-repeat;"
	></div>
	<img
		src={Cracks}
		alt=""
		class="absolute top-1/2 -translate-y-1/2 opacity-30 mix-blend-color-burn"
	/>
</section>
