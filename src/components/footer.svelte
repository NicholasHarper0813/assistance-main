<script>
	import FooterBg from '$lib/images/footer-bg.png';
	import Logo from '$lib/svg/logo.svg';
</script>

<footer class="relative">
	<div class="container-custom mx-auto">
		<div class="mb-10 flex justify-center">
			<h2 class="bg-primary font-victor text-center text-2xl font-medium italic md:text-left">
				Solana Foundation Hackathon Official Rules
			</h2>
		</div>
		<div class="relative z-10 mx-8 mb-28 sm:mx-auto xl:w-[34vw]">
			<p class="text-dark2 text-center text-sm leading-relaxed">
				The Solana Renaissance Hackathon is a competition where projects will be evaluated by judges
				on their technological merits without consideration of legal viability. Participants in the
				Hackathon will create software solely for purposes of evaluation by judges as part of a
				competition and not for commercial deployment or release as part of the Hackathon. All
				participants must comply with applicable laws and regulations when releasing any software
				that they develop as part of the Hackathon.
			</p>
			<p class="text-dark2 mt-8 text-center text-sm leading-relaxed">
				The developer resources that Solana Foundation (“SF”) provides are for educational and
				inspirational purposes only. SF does not encourage, induce or sanction the deployment of any
				such applications in violation of applicable laws or regulations. SF does not encourage,
				induce or sanction the deployment, integration or use of any such applications (including
				the code comprising the Solana blockchain protocol) in violation of applicable laws or
				regulations and hereby prohibits any such deployment, integration or use. This includes use
				of any such applications by the reader (a) in violation of export control or sanctions laws
				of the United States or any other applicable jurisdiction, (b) if the reader is located in
				or ordinarily resides in a country or territory subject to comprehensive sanctions
				administered by the U.S. Office of Foreign Assets Control (OFAC), (c) if the reader is or is
				working on behalf of a Specially Designated National (SDN) or is a person subject to similar
				blocking or denied party prohibitions, or (d) in violation of the Commodities and Exchange
				Act.
			</p>
		</div>
		<div class="relative z-10 mx-auto max-w-2xl pb-20 md:pt-12 xl:pt-0">
			<ul class="grid grid-cols-5 font-medium">
				<li class="flex items-center justify-center py-2">
					<a class="inline-block text-sm duration-300 hover:opacity-75 md:text-base" href="/">
						Resources
					</a>
				</li>
				<li class="flex items-center justify-center py-2">
					<a class="inline-block text-sm duration-300 hover:opacity-75 md:text-base" href="/">
						FAQs
					</a>
				</li>
				<li class="flex items-center justify-center py-2">
					<a class="inline-block text-sm duration-300 hover:opacity-75 md:text-base" href="/">
						<img src={Logo} alt="" class="w-8 shrink-0 md:w-auto" />
					</a>
				</li>
				<li class="flex items-center justify-center py-2">
					<a class="inline-block text-sm duration-300 hover:opacity-75 md:text-base" href="/">
						Accelerator
					</a>
				</li>
				<li class="flex items-center justify-center py-2">
					<a class="inline-block text-sm duration-300 hover:opacity-75 md:text-base" href="/">
						Register
					</a>
				</li>
			</ul>
		</div>
	</div>
	<div class="absolute bottom-0 left-0 right-0 hidden overflow-hidden sm:block">
		<div class="flex justify-center">
			<img src={FooterBg} alt="" class="w-full min-w-[1400px]" />
		</div>
	</div>
</footer>
