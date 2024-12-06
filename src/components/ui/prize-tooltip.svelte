<script lang="ts">
  import Logo from "../icons/logo.svelte";

  export let className: string = "";
</script>

<div
  class={"border bg-[#F6F6F6] absolute bottom-full left-full w-[440px] min-h-[100px] flex " +
    className}
>
  <div class="border m-[2px] bg-white flex grow gap-4">
    <div class="shrink-0 flex flex-col justify-between">
      <Logo className="w-6 mt-2 ml-1" />
      <svg
        xmlns="http://www.w3.org/2000/svg"
        width="36"
        height="36"
        viewBox="0 0 36 36"
        fill="none"
      >
        <rect width="36" height="36" fill="#A8EAFF" />
        <path d="M8 18H28" stroke="#191817" stroke-width="2" />
      </svg>
    </div>
    <div class="p-2 py-4 text-lg">
      Plus 3 passes to the next upcoming Solana Breakpoint 2024 conference,
      where you may present your project to the Solana community.
    </div>
  </div>
</div>
