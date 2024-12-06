<script lang="ts">
  import { slide } from "svelte/transition";
  import Logo from "../icons/logo.svelte";

  export let index: number;
  export let show: number | null;
  export let showCollapse: (index: number) => void;
  export let item: string;
</script>

<button
  class="border bg-[#F6F6F6] mt-10 w-full"
  style="top: calc(100% + 8px)"
  on:click={() => showCollapse(index)}
>
  <div
    class={"border m-[2px] font-medium flex flex-col " +
      (show === index ? "bg-dark1 text-white" : "bg-white text-dark1")}
  >
    <button class="py-3 px-5 w-full flex justify-between items-center">
      <div class="flex items-center">
        <Logo className="h-4 shrink-0" />
        {item}
      </div>
      <svg
        xmlns="http://www.w3.org/2000/svg"
        width="20"
        height="20"
        viewBox="0 0 20 20"
        fill="none"
      >
        <path
          d="M16.6673 7.5L10.0007 14.1667L3.33398 7.5"
          stroke="currentColor"
          stroke-width="2"
        />
      </svg>
    </button>
  </div>
</button>
{#if show === index}
  <div transition:slide>
    <slot />
  </div>
{/if}
