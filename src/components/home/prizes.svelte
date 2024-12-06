<script lang="ts">
	// Components
	import Title from '../ui/title.svelte';
	import PrizeTooltip from '../ui/prize-tooltip.svelte';
	//   Images
	import PrizesClouds from '$lib/images/prizes-clouds.png';
	import PrizesCenter from '$lib/images/prizes-center.png';
	import PrizeQuadrant from '$lib/images/prizes-quadrant.png';
	import Cracks from '$lib/images/cracks.png';
</script>

<section
	class="relative overflow-x-hidden bg-cover py-40 sm:mt-0 md:pb-40 md:pt-96"
	style="background: linear-gradient(180deg, #FEFCF9 0%, rgba(254, 252, 249, 0.00) 51%, #FEFCF9 100%), url({PrizesClouds}), lightgray 50% / cover no-repeat; "
>
	<div class="container-custom relative z-10 mx-auto">
		<div class="relative hidden sm:block">
			<div class="absolute left-0 top-0 w-full">
				<Title>
					<span class="bg-primary">Prizes</span>
				</Title>
			</div>
			<div class="grid grid-cols-3">
				<!-- Row 1 -->
				<div></div>
				<div class="flex items-center justify-center">
					<div class="relative flex items-center justify-center">
						<img src={PrizeQuadrant} alt="" class="rotate-90" />
						<div class="absolute">
							<p class="font-victor text-dark2 mb-4 font-semibold italic">USDC</p>
							<div class="group relative cursor-pointer">
								<h3 class="bg-dark2 font-inter text-7xl font-semibold text-white 2xl:text-8xl">
									$50K
								</h3>
								<PrizeTooltip className="opacity-0 group-hover:opacity-100 duration-300" />
							</div>
							<p
								class="font-victor bg-primary text-dark2 w-min whitespace-nowrap text-2xl italic 2xl:text-3xl"
							>
								Grand Champion
							</p>
						</div>
					</div>
				</div>
				<div></div>
				<!-- Row 2 -->
				<div class="flex items-center justify-center">
					<div class="relative flex items-center justify-center">
						<img src={PrizeQuadrant} alt="" />
						<div class="absolute">
							<p class="font-victor text-dark2 mb-4 font-semibold italic">USDC</p>
							<div class="group relative cursor-pointer">
								<h3 class="bg-dark2 font-inter text-7xl font-semibold text-white 2xl:text-8xl">
									$10K
								</h3>
								<PrizeTooltip className="opacity-0 group-hover:opacity-100 duration-300 z-20" />
							</div>
							<p
								class="font-victor bg-primary text-dark2 w-min whitespace-nowrap text-2xl italic 2xl:text-3xl"
							>
								Public Goods Award
							</p>
						</div>
					</div>
				</div>
				<div>
					<img src={PrizesCenter} alt="" class="relative z-10 scale-[1.15]" />
				</div>
				<div class="flex items-center justify-center">
					<div class="relative flex items-center justify-center">
						<img src={PrizeQuadrant} alt="" class="rotate-180" />
						<div class="absolute">
							<p class="font-victor text-dark2 mb-4 font-semibold italic">USDC</p>
							<div class="group relative cursor-pointer">
								<h3 class="bg-dark2 font-inter text-7xl font-semibold text-white 2xl:text-8xl">
									$5K
								</h3>
								<PrizeTooltip
									className="opacity-0 group-hover:opacity-100 duration-300 z-20 left-[50%]"
								/>
							</div>
							<p
								class="font-victor bg-primary text-dark2 w-min whitespace-nowrap text-2xl italic 2xl:text-3xl"
							>
								Climate Award
							</p>
						</div>
					</div>
				</div>
				<!-- Row 3 -->
				<div></div>
				<div class="flex items-center justify-center">
					<div class="relative flex items-center justify-center">
						<img src={PrizeQuadrant} alt="" class="-rotate-90" />
						<div class="absolute">
							<p class="font-victor text-dark2 mb-4 font-semibold italic">USDC</p>
							<div class="group relative cursor-pointer">
								<h3 class="bg-dark2 font-inter text-7xl font-semibold text-white 2xl:text-8xl">
									$10K
								</h3>
								<PrizeTooltip className="opacity-0 group-hover:opacity-100 duration-300 z-20" />
							</div>
							<p
								class="font-victor bg-primary text-dark2 w-min whitespace-nowrap text-2xl italic 2xl:text-3xl"
							>
								University Award
							</p>
						</div>
					</div>
				</div>
				<div></div>
			</div>
		</div>

		<!-- this div is for small screens -->
		<div class="block sm:hidden">
			<div class="">
				<h2 class="font-victor relative text-7xl italic leading-none">
					<span class="bg-primary">Prizes</span>
				</h2>
			</div>
			<div>
				<div class="mt-8 flex flex-col gap-6">
					<div>
						<img src={PrizesCenter} alt="" />
					</div>
					<div class="relative flex items-center justify-center">
						<img src={PrizeQuadrant} alt="" class="rotate-90" />
						<div class="absolute">
							<p class="font-victor text-dark2 mb-4 font-semibold italic">USDC</p>
							<h3 class="bg-dark2 font-inter text-7xl font-semibold text-white">$50K</h3>
							<p class="font-victor bg-primary text-dark2 w-min whitespace-nowrap text-2xl italic">
								Grand Champion
							</p>
						</div>
					</div>
					<div class="relative flex items-center justify-center">
						<img src={PrizeQuadrant} alt="" class="rotate-90" />
						<div class="absolute">
							<p class="font-victor text-dark2 mb-4 font-semibold italic">USDC</p>
							<h3 class="bg-dark2 font-inter text-7xl font-semibold text-white">$10K</h3>
							<p class="font-victor bg-primary text-dark2 w-min whitespace-nowrap text-2xl italic">
								Public Goods Award
							</p>
						</div>
					</div>
					<div class="relative flex items-center justify-center">
						<img src={PrizeQuadrant} alt="" class="rotate-90" />
						<div class="absolute">
							<p class="font-victor text-dark2 mb-4 font-semibold italic">USDC</p>
							<h3 class="bg-dark2 font-inter text-7xl font-semibold text-white">$5K</h3>
							<p class="font-victor bg-primary text-dark2 w-min whitespace-nowrap text-2xl italic">
								Climate Award
							</p>
						</div>
					</div>
					<div class="relative flex items-center justify-center">
						<img src={PrizeQuadrant} alt="" class="rotate-90" />
						<div class="absolute">
							<p class="font-victor text-dark2 mb-4 font-semibold italic">USDC</p>
							<h3 class="bg-dark2 font-inter text-7xl font-semibold text-white">$10K</h3>
							<p class="font-victor bg-primary text-dark2 w-min whitespace-nowrap text-2xl italic">
								University Award
							</p>
						</div>
					</div>
				</div>
			</div>
		</div>
	</div>

	<img
		src={Cracks}
		alt=""
		class="absolute top-1/2 -translate-y-1/2 opacity-30 mix-blend-color-burn"
	/>
</section>
