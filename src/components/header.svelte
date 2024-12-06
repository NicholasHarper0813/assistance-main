<script lang="ts">
  import Logo from "$lib/svg/logo.svg";

  import { fade } from "svelte/transition";

  let isMenuOpen = false;
</script>

<header class="py-10 flex justify-center items-center">
  <nav class="hidden md:block">
    <div class="border bg-[#F6F6F6]">
      <div
        class="flex items-center border m-[2px] bg-white font-medium gap-1 relative"
      >
        <a
          href="/"
          class="py-3 w-[134px] hover:bg-[#D9D9D9] duration-300 text-center"
          >Resources</a
        >
        <a
          href="/"
          class="py-3 w-[134px] hover:bg-[#D9D9D9] duration-300 text-center mr-20"
          >Accelerator</a
        >
        <div
          class="border bg-white flex h-20 w-20 absolute left-1/2 -translate-x-1/2"
        >
          <div
            class="border m-[2px] grow flex items-center justify-center bg-[#D9D9D9]/25"
          >
            <img src={Logo} alt="" srcset="" />
          </div>
        </div>
        <a
          href="/"
          class="py-3 w-[134px] hover:bg-[#D9D9D9] duration-300 text-center"
          >FAQs</a
        >
        <a
          href="/"
          class="py-3 w-[134px] text-center bg-primary font-victor hover:bg-dark1 hover:text-white duration-500"
          >Register Now</a
        >
      </div>
    </div>
  </nav>

  <!-- Mobile Nav -->
  <nav class="md:hidden relative">
    <div class="border bg-[#F6F6F6]">
      <div
        class="flex items-center border m-[2px] bg-white font-medium gap-1 relative"
      >
        <button
          class="py-3 w-[110px] mr-20 text-base flex items-center justify-center gap-2"
          on:click={() => (isMenuOpen = !isMenuOpen)}
        >
          <svg
            xmlns="http://www.w3.org/2000/svg"
            fill="none"
            viewBox="0 0 24 24"
            stroke-width="1.5"
            stroke="currentColor"
            class="w-5 h-5"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5"
            />
          </svg>

          <span>Menu</span>
        </button>

        <div
          class="border bg-white flex h-20 w-20 absolute left-1/2 -translate-x-1/2"
        >
          <div class="border m-[2px] grow flex items-center justify-center">
            <img src={Logo} alt="" srcset="" />
          </div>
        </div>
        <a
          href="/"
          class="py-3 w-[110px] text-center bg-primary italic font-normal font-instrument"
          >Register</a
        >
      </div>
    </div>

    {#if isMenuOpen}
      <div
        transition:fade={{ duration: 100 }}
        class="border bg-[#F6F6F6] absolute left-0 right-0"
        style="top: calc(100% + 8px)"
      >
        <div class="border m-[2px] bg-white font-medium flex flex-col">
          <a href="/" class="py-3 w-full text-center">Resources</a>
          <a href="/" class="py-3 w-full text-center">Accelerator</a>
          <a href="/" class="py-3 w-full text-center">FAQs</a>
        </div>
      </div>
    {/if}
  </nav>
</header>
