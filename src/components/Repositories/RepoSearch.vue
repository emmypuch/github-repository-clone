<template>
  <div class="flex gap-4">
    <div class="input w-full">
      <input
        type="text"
        placeholder="Find a repository..."
        class="rounded-lg border border-gray-400 text-[0.9rem] text-gray-500 px-[15px] py-[5px] w-full"
      />
    </div>
    <div class="flex gap-2">
      <div>
        <a
          href="#"
          class="flex gap-[3px] bg-gray-100 border border-gray-400 px-[15px] py-[5px] rounded-lg"
        >
          <p class="text-[#1F2329] text-[0.9rem]">Type</p>
          <img src="/src/assets/images/chevron-down.svg" alt="" class="w-3 h-3 mt-[5px]" />
        </a>
      </div>
      <div>
        <a
          href="#"
          class="flex gap-[3px] bg-gray-100 border border-gray-400 px-[15px] text-center py-[6px] rounded-lg"
        >
          <p class="text-[#1F2329] text-[0.9rem]">Language</p>
          <img src="/src/assets/images/chevron-down.svg" alt="" class="w-3 h-3 mt-[5px]" />
        </a>
      </div>
      <div>
        <a
          href="#"
          class="flex gap-[3px] bg-gray-100 border border-gray-400 px-[15px] text-center py-[6px] rounded-lg"
        >
          <p class="text-[#1F2329] text-[0.9rem]">Sort</p>
          <img src="/src/assets/images/chevron-down.svg" alt="" class="w-3 h-3 mt-[5px]" />
        </a>
      </div>
      <div>
        <a href="#" class="flex gap-[3px] bg-[#1E883E] px-[15px] text-center py-[6px] rounded-lg">
          <img src="/src/assets/images/rep.svg" alt="" class="w-3 h-3 mt-[5px]" />
          <p class="text-[#f2f7f3] text-[0.9rem]">New</p>
        </a>
      </div>
    </div>
  </div>
</template>
