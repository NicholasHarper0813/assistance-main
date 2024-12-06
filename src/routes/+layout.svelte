<script>
  import { onMount } from "svelte";
  import "../app.css";

  let windowWidth = 0;

  onMount(() => {
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

<div class="max-w-[2400px] mx-auto relative">
  <slot />

  {#if windowWidth > 2400}
    <div
      class="absolute h-full w-20 z-[1000] left-0 top-0"
      style="background: linear-gradient(to right, #FEFCF9, transparent);"
    />
    <div
      class="absolute h-full w-20 z-[1000] right-0 top-0"
      style="background: linear-gradient(to left, #FEFCF9, transparent);"
    />
  {/if}
</div>
