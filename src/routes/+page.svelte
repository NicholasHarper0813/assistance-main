<script lang="ts">
  // Components
  import Header from "../components/header.svelte";
  import Footer from "../components/footer.svelte";
  import Tracks from "../components/home/tracks.svelte";

  // Images
  import BgClouds from "$lib/images/bgClouds.png";
  import FooterClouds from "$lib/images/footer-clouds.png";
  import HeroElements from "$lib/images/hero-elements.png";
  import Judges from "../components/home/judges.svelte";
  import Accelerator from "../components/home/accelerator.svelte";
  import Prizes from "../components/home/prizes.svelte";
  import ElementCracks from "$lib/images/elementCracks.png";

  import { onMount } from "svelte";
  import TracksSmall from "../components/home/tracks-small.svelte";
  import Modal from "../components/ui/modal.svelte";
  import SolanaFoundation from "../components/icons/solana-foundation.svelte";
  import Colosseum from "../components/icons/colosseum.svelte";
  import Hero from "../components/home/hero.svelte";
  import FooterTop from "../components/footer-top.svelte";

  let windowWidth = 0;
  let showModal = false;

  onMount(() => {
    windowWidth = window.innerWidth;
    window.addEventListener("resize", () => {
      windowWidth = window.innerWidth;
    });

    return () => {
      window.removeEventListener("resize", () => {
        windowWidth = window.innerWidth;
      });
    };
  });
</script>

<div>
  <div
    style="background-image: url({BgClouds}); background-position: center top;"
    class="bg-cover relative"
  >
    <div class="relative z-10">
      <Header />
      <Hero />
      <section
        class="overflow-x-hidden flex justify-center relative z-10 pt-24 md:pt-0 md:mt-24"
      >
        <div class="absolute left-0 right-0 top-0 sm:hidden">
          <div class="px-8 flex justify-between items-center">
            <div>
              <p class="mb-4">Hosted By</p>
              <SolanaFoundation className="w-32" />
            </div>
            <div>
              <p class="mb-4">Powered By</p>
              <Colosseum className="w-32" />
            </div>
          </div>
        </div>
        <!-- svelte-ignore a11y-click-events-have-key-events -->
        <!-- svelte-ignore a11y-no-noninteractive-element-interactions -->
        <img
          src={HeroElements}
          alt=""
          class="lg:w-full min-w-[1000px]"
          on:click={() => {
            showModal = true;
          }}
        />
      </section>
    </div>
    <div class="absolute top-0 left-0 right-0">
      <div class="container-custom mx-auto">
        <img src={ElementCracks} alt="" class="w-full opacity-40" />
      </div>
    </div>
  </div>

  <!-- Accelerator -->
  <Accelerator />

  <!-- Prizes -->
  <Prizes />

  <!-- Tracks -->
  {#if windowWidth > 1024}
    <Tracks />
  {:else}
    <TracksSmall />
  {/if}

  <!-- Judges -->
  <Judges />

  <!-- Footer -->
  <div
    class="bg-cover bg-bottom"
    style="background-image: url({FooterClouds});"
  >
    <FooterTop />
    <Footer />
  </div>
</div>

<Modal bind:showModal>
  <div class="aspect-video w-full">
    <iframe
      width="100%"
      height="100%"
      src="https://www.youtube.com/embed/HXcJM0mOp40?si=b6kENEYxfnBpc_ZR"
      title="YouTube video player"
      frameborder="0"
      allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
      allowfullscreen
    ></iframe>
  </div>
</Modal>

<style></style>
