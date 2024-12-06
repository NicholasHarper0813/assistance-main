<script lang="ts">
	// Images
	import SolanaLogo from '$lib/svg/solana-logo.svg';
	import TracksContainer from '$lib/images/tracks-container.png';
	import DePinTrack from '$lib/images/depin-track.png';
	import DeFiTrack from '$lib/images/defi-track.png';
	import GamingTrack from '$lib/images/gaming-track.png';
	import ConsumerTrack from '$lib/images/consumer-track.png';
	import InfrastructureTrack from '$lib/images/infrastructure-track.png';
	import Accordion from '../ui/accordion.svelte';
	import Title from '../ui/title.svelte';

	let activeImage = DePinTrack;

	function renderImages(tab: string) {
		switch (tab) {
			case 'DePin':
				activeImage = DePinTrack;
				break;
			case 'DeFi':
				activeImage = DeFiTrack;
				break;
			case 'Payments':
				activeImage = DePinTrack;
				break;
			case 'Consumer Apps':
				activeImage = ConsumerTrack;
				break;
			case 'Gaming':
				activeImage = GamingTrack;
				break;
			case 'Infrastructure':
				activeImage = InfrastructureTrack;
				break;
		}
	}

	let show: number | null = 0;
	const items = ['DePin', 'DeFi', 'Payments', 'Consumer Apps', 'Gaming', 'Infrastructure'];

	const showCollapse = (i: number) => {
		i === show ? (show = null) : (show = i);
		renderImages(items[i]);
	};
</script>

<section class="py-24">
	<div class="container-custom mx-auto">
		<div class="relative">
			<div class="relative z-10 flex gap-10">
				<Title>
					<span class="bg-primary">Tracks</span>
				</Title>
			</div>
			{#each items as item, i}
				<Accordion index={i} {item} {show} {showCollapse}>
					<div class="mt-10">
						<h2 class="text-6xl font-semibold">
							{show !== null && show >= 0 && items[show]}
						</h2>
						<p class="mt-6 text-2xl font-medium">
							Design crypto incentivizes to build physical infrastructure networks to disrupt
							traditional incumbents.
						</p>
					</div>
					<div>
						<p class="mt-6 text-lg">Presented by</p>
						<img src={SolanaLogo} alt="" srcset="" />
					</div>
					<div class="relative mt-10 flex items-center justify-center">
						<img src={TracksContainer} alt="" />
						<img src={activeImage} alt="" class="absolute" />
					</div>
					<ul class="mt-10 flex w-full flex-col gap-6">
						<li class="flex items-center justify-between">
							<div class="font-instrument flex items-center gap-4">
								<span
									class="text-dark1 bg-primary flex h-[32px] w-[40px] items-center justify-center rounded-full italic"
									>I</span
								>
								<span class="text-[20px]">First Prize</span>
							</div>
							<div class="text-2xl font-semibold">$30,000</div>
						</li>
						<li class="flex items-center justify-between">
							<div class="font-instrument flex items-center gap-4">
								<span
									class="text-dark1 bg-primary flex h-[32px] w-[40px] items-center justify-center rounded-full italic"
									>II</span
								>
								<span class="text-[20px]">Second Prize</span>
							</div>
							<div class="text-2xl font-semibold">$20,000</div>
						</li>
						<li class="flex items-center justify-between">
							<div class="font-instrument flex items-center gap-4">
								<span
									class="text-dark1 bg-primary flex h-[32px] w-[40px] items-center justify-center rounded-full italic"
									>III</span
								>
								<span class="text-[20px]">Third Prize</span>
							</div>
							<div class="text-2xl font-semibold">$15,000</div>
						</li>
						<li class="flex items-center justify-between">
							<div class="font-instrument flex items-center gap-4">
								<span
									class="text-dark1 bg-primary flex h-[32px] w-[40px] items-center justify-center rounded-full italic"
									>IV</span
								>
								<span class="text-[20px]">Fourth Prize</span>
							</div>
							<div class="text-2xl font-semibold">$10,000</div>
						</li>
						<li class="flex items-center justify-between">
							<div class="font-instrument flex items-center gap-4">
								<span
									class="text-dark1 bg-primary flex h-[32px] w-[40px] items-center justify-center rounded-full italic"
									>V</span
								>
								<span class="text-[20px]">Fifth Prize</span>
							</div>
							<div class="text-2xl font-semibold">$5,000</div>
						</li>
					</ul>
				</Accordion>
			{/each}
		</div>
	</div>
</section>
