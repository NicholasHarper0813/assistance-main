<script lang="ts">
	// Components
	import TrackTabBtn from '../ui/track-tab-btn.svelte';

	// Images
	import SolanaLogo from '$lib/svg/solana-logo.svg';
	import TracksContainer from '$lib/images/tracks-container.png';
	import TrackLeft from '$lib/svg/track-bottom-left.svg';
	import TrackRight from '$lib/svg/track-top-right.svg';
	import DePinTrack from '$lib/images/depin-track.png';
	import DeFiTrack from '$lib/images/defi-track.png';
	import GamingTrack from '$lib/images/gaming-track.png';
	import ConsumerTrack from '$lib/images/consumer-track.png';
	import InfrastructureTrack from '$lib/images/infrastructure-track.png';
	import Title from '../ui/title.svelte';

	const trackTabs = ['DePin', 'DeFi', 'Payments', 'Consumer Apps', 'Gaming', 'Infrastructure'];
	let activeTab = 'DePin';
	let activeImage = DePinTrack;

	function changeActiveTab(tab: string) {
		activeTab = tab;
		renderImages(tab);
	}

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
</script>

<section class="py-24">
	<div class="container-custom mx-auto">
		<div class="relative">
			<div class="relative z-10 mb-20 flex gap-10">
				<Title>
					<span class="bg-primary">Tracks</span>
				</Title>
				<div class="flex max-w-3xl flex-wrap gap-6">
					{#each trackTabs as tab}
						<button on:click={() => changeActiveTab(tab)}>
							<TrackTabBtn title={tab} active={tab === activeTab} />
						</button>
					{/each}
				</div>
			</div>
			<div class="grid grid-cols-12 gap-4">
				<div class="col-span-12 flex flex-col justify-between py-10 pl-10 sm:col-span-3">
					<div>
						<h2 class="text-5xl font-semibold 2xl:text-6xl">{activeTab}</h2>
						<p class="mt-6 text-xl font-medium 2xl:text-2xl">
							Design crypto incentivizes to build physical infrastructure networks to disrupt
							traditional incumbents.
						</p>
					</div>
					<div>
						<p>Presented by</p>
						<img src={SolanaLogo} alt="" srcset="" />
					</div>
				</div>
				<div class="col-span-12 flex items-center justify-center sm:col-span-6">
					<div class="relative flex w-[70%] items-center justify-center 2xl:w-[90%]">
						<img src={TracksContainer} alt="" class="w-full" />
						<img src={activeImage} alt="" class="absolute w-[55%]" />
					</div>
				</div>
				<div class="col-span-12 flex items-end whitespace-nowrap py-10 pr-10 sm:col-span-3">
					<ul class="flex w-full flex-col gap-6">
						<li class="flex items-center justify-between">
							<div class="font-victor flex items-center gap-4">
								<span
									class="text-dark1 bg-primary flex h-[32px] w-[40px] items-center justify-center rounded-full italic"
									>I</span
								>
								<span class="text-lg 2xl:text-[20px]">First Prize</span>
							</div>
							<div class="text-lg font-semibold 2xl:text-2xl">$30,000</div>
						</li>
						<li class="flex items-center justify-between">
							<div class="font-victor flex items-center gap-4">
								<span
									class="text-dark1 bg-primary flex h-[32px] w-[40px] items-center justify-center rounded-full italic"
									>II</span
								>
								<span class="text-lg 2xl:text-[20px]">Second Prize</span>
							</div>
							<div class="text-lg font-semibold 2xl:text-2xl">$20,000</div>
						</li>
						<li class="flex items-center justify-between">
							<div class="font-victor flex items-center gap-4">
								<span
									class="text-dark1 bg-primary flex h-[32px] w-[40px] items-center justify-center rounded-full italic"
									>III</span
								>
								<span class="text-lg 2xl:text-[20px]">Third Prize</span>
							</div>
							<div class="text-lg font-semibold 2xl:text-2xl">$15,000</div>
						</li>
						<li class="flex items-center justify-between">
							<div class="font-victor flex items-center gap-4">
								<span
									class="text-dark1 bg-primary flex h-[32px] w-[40px] items-center justify-center rounded-full italic"
									>IV</span
								>
								<span class="text-lg 2xl:text-[20px]">Fourth Prize</span>
							</div>
							<div class="text-lg font-semibold 2xl:text-2xl">$10,000</div>
						</li>
						<li class="flex items-center justify-between">
							<div class="font-victor flex items-center gap-4">
								<span
									class="text-dark1 bg-primary flex h-[32px] w-[40px] items-center justify-center rounded-full italic"
									>V</span
								>
								<span class="text-lg 2xl:text-[20px]">Fifth Prize</span>
							</div>
							<div class="text-lg font-semibold 2xl:text-2xl">$5,000</div>
						</li>
					</ul>
				</div>
			</div>

			<img src={TrackLeft} alt="" class="absolute bottom-0 left-0 hidden md:block" />
			<img src={TrackRight} alt="" class="absolute right-0 top-0" />
		</div>
	</div>
</section>
