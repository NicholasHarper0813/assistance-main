<script lang="ts">
	// Images
	import HeroTitle from '$lib/svg/hero-title.svg';
	import HeroTitleSmall from '$lib/svg/hero-title-small.svg';

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

<section>
	<div class="container-custom mx-auto mt-4">
		<img
			src={windowWidth < TAB_WIDTH ? HeroTitleSmall : HeroTitle}
			alt=""
			srcset=""
			class="w-full"
		/>
	</div>

	<div class="container-custom mx-auto pb-[102px] pt-[72px]">
		<div class="grid items-start md:grid-cols-2 lg:gap-24 2xl:gap-40">
			<div>
				<h2
					class="text-dark1 text-center text-lg font-medium leading-snug md:text-left xl:text-2xl 2xl:text-[28px]"
				>
					Start building the next breakout startup and bring the crypto ecosystem into the Golden
					Age.
				</h2>
				<button
					class="bg-dark1 font-victor hover:bg-primary hover:text-dark1 mt-8 hidden items-center gap-2 px-8 py-4 text-2xl italic text-white duration-500 md:flex"
				>
					Register now
					<svg
						xmlns="http://www.w3.org/2000/svg"
						width="16"
						height="14"
						viewBox="0 0 16 14"
						fill="none"
					>
						<path
							d="M9.77734 0.777832C9.77734 4.21427 12.5631 7.00005 15.9996 7.00005C12.5631 7.00005 9.77734 9.78584 9.77734 13.2223"
							stroke="currentColor"
							stroke-width="2"
						/>
						<rect y="6.11108" width="13.3333" height="1.77778" fill="currentColor" />
					</svg>
				</button>
			</div>
			<div class="mt-6 flex items-center justify-center gap-5 md:mt-0 md:justify-end md:gap-9">
				<div>
					<h4 class="font-instrument text-3xl italic xl:text-5xl 2xl:text-7xl">
						{windowWidth > TAB_WIDTH ? 'March 4' : 'March 4, 24'}
					</h4>
					<p class="mt-2 hidden text-lg font-medium md:block xl:text-2xl">2024</p>
				</div>
				<div class="bg-dark1 h-[1px] w-8 opacity-35"></div>
				<div>
					<h4 class="font-instrument text-3xl italic xl:text-5xl 2xl:text-7xl">
						{windowWidth > TAB_WIDTH ? 'April 8' : 'April 8, 24'}
					</h4>
					<p class="mt-2 hidden text-lg font-medium md:block xl:text-2xl">2024</p>
				</div>
			</div>

			<button
				class="bg-dark1 font-instrument hover:bg-primary hover:text-dark1 mt-8 flex items-center justify-between gap-2 px-8 py-4 text-xl italic text-white duration-500 md:hidden"
			>
				Register Now
				<svg
					xmlns="http://www.w3.org/2000/svg"
					width="16"
					height="14"
					viewBox="0 0 16 14"
					fill="none"
				>
					<path
						d="M9.77734 0.777832C9.77734 4.21427 12.5631 7.00005 15.9996 7.00005C12.5631 7.00005 9.77734 9.78584 9.77734 13.2223"
						stroke="currentColor"
						stroke-width="2"
					/>
					<rect y="6.11108" width="13.3333" height="1.77778" fill="currentColor" />
				</svg>
			</button>
		</div>
	</div>
</section>
