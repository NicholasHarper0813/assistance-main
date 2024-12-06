<script lang="ts">
  export let image: string;
  export let number: number;
  export let title: string;
  export let subtitle: string;
</script>

<div class="flex flex-col md:items-center xl:items-start">
  <div class="relative">
    <img src={image} alt="" />
    <div
      class="w-[38px] h-[50px] text-[20px] text-white font-victor bg-dark1 rounded-full absolute top-0 left-0 flex items-center justify-center outline outline-offset-2 outline-[#D5CCC0] outline-2 border border-[#D5CCC0]"
    >
      {number}
    </div>
  </div>
  <h3 class="text-4xl md:text-7xl font-semibold font-inter mt-10">{title}</h3>
  <h5 class="text-xl md:text-2xl font-medium mt-2 text-dark2 xl:text-left">
    {subtitle}
  </h5>
</div>
