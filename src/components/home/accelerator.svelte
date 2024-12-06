<script lang="ts">
	//   Images
	import PreSeed from '$lib/images/prize-img-1.png';
	import Network from '$lib/svg/prize-img-2.svg';
	import Mentorship from '$lib/svg/prize-img-3.svg';
	import BgCloud from '$lib/images/bg-cloud-single.png';
	import Title from '../ui/title.svelte';
	import AcceleratorCard from '../ui/accelerator-card.svelte';
</script>

<section class="relative pt-40">
	<div class="container-custom relative z-[10] mx-auto">
		<div class="mb-20 grid xl:grid-cols-2 2xl:grid-cols-3">
			<div class="2xl:col-span-2">
				<div class="flex">
					<p
						class="text-dark2 relative mb-10 flex items-center text-[20px] font-medium after:absolute after:left-[120%] after:h-[1px] after:w-16 after:bg-[#BDBDBD] after:content-[''] md:text-2xl md:after:w-24"
					>
						Now introducing
					</p>
				</div>
				<Title>
					<span class="bg-primary inline-block">Colosseum's</span><br /><span
						class="bg-primary inline-block">Accelerator</span
					>
				</Title>
			</div>
			<div class="flex items-end">
				<p class="text-dark2 mt-12 text-[20px] font-medium md:text-2xl">
					All hackathon winners will be interviewed and considered for Colosseum's accelerator
					program. Accepted teams will receive:
				</p>
			</div>
		</div>
		<div
			class="mt-28 grid justify-center gap-x-20 gap-y-28 xl:h-[1000px] xl:grid-cols-3 xl:justify-start"
		>
			<div class="flex items-start">
				<AcceleratorCard
					number={1}
					image={PreSeed}
					title="$250,000"
					subtitle="in pre-seed funding"
				/>
			</div>

			<div class="flex items-center">
				<AcceleratorCard
					number={2}
					image={Network}
					title="Network"
					subtitle="Exclusive access to an elite founder network"
				/>
			</div>
			<div class="flex items-end">
				<AcceleratorCard
					number={3}
					image={Mentorship}
					title="Mentorship"
					subtitle="Direct ecosystem connections and 1:1 mentorship."
				/>
			</div>
		</div>
	</div>
	<img src={BgCloud} alt="" class="absolute right-0 top-0" />
	<img src={BgCloud} alt="" class="absolute bottom-0 left-0" />
</section>
