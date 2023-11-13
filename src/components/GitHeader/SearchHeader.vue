<template>
  <div>
    <div class="desktop hidden md:flex md:justify-between">
      <div class="flex justify-center gap-2">
        <div class="mt-1">Menu</div>
        <div>
          <img src="/src/assets/images/github.svg" alt="" class="w-8 h-8 rounded-[50%]" />
        </div>
        <div class="user hover:bg-[#DDE3E8] px-[3px] py-[5px] rounded-lg">
          <p class="text-center text-sm text-[#1F2329]">emmypuch</p>
        </div>
      </div>
      <div class="flex mt-2 md:mt-0">
        <ul class="flex gap-3">
          <li class="border-solid border-[1px] border-gray-400 rounded-lg hover:bg-[#DDE3E8]">
            <router-link
              to="#"
              class="no-underline flex items-center text-center text-[12px] text-gray-500 px-3 py-[5px]"
            >
              <img src="/src/assets/images/search.png" alt="" class="w-3 h-3 mr-2" />
              Type
              <span
                class="border-[1px] border-gray-400 rounded-md px-[5px] py-[3px] text-xs ml-1 mr-1"
              >
                /
              </span>

              to search
              <div class="flex ml-5">
                <img src="/src/assets/images/chevron-right.svg" alt="" class="w-3 h-3" />
              </div>
            </router-link>
          </li>
          <li
            class="border-solid border-[1px] border-gray-400 rounded-lg p-[10px] hover:bg-[#DDE3E8]"
          >
            <div class="flex gap-2">
              <img src="/src/assets/images/plus.svg" alt="" class="w-3 h-3" />
              <img src="/src/assets/images/chevron-down.svg" alt="" class="w-3 h-3" />
            </div>
          </li>
          <li
            class="border-solid border-[1px] border-gray-400 rounded-lg p-[5px] hover:bg-[#DDE3E8]"
          >
            <img src="/src/assets/images/issue.svg" alt="" class="w-3 h-3 mr-2" />
          </li>
          <li class="">
            <img
              src="/src/assets/images/tihanapic.png"
              alt=""
              class="w-10 h-10 mr-2 rounded-[50%]"
            />
          </li>
        </ul>
      </div>
    </div>

    <!-- Mobile -->
    <div class="mobile md:hidden flex justify-between">
      <div class="flex justify-center gap-2">
        <div class="mt-1">Menu</div>
        <div>
          <img src="/src/assets/images/github.svg" alt="" class="w-8 h-8 rounded-[50%]" />
        </div>
        <div
          class="user text-center hover:bg-[#DDE3E8] px-[3px] py-[5px] rounded-lg text-sm text-[#1F2329]"
        >
          emmypuch
        </div>
      </div>
      <div class="flex">
        <div class="flex gap-3">
          <img src="/src/assets/images/tihanapic.png" alt="" class="w-8 h-8 mr-2 rounded-[50%]" />
        </div>
        <div class="flex gap-3">
          <img src="/src/assets/images/tihanapic.png" alt="" class="w-8 h-8 mr-2 rounded-[50%]" />
        </div>
        <div class="flex gap-3">
          <img src="/src/assets/images/tihanapic.png" alt="" class="w-8 h-8 mr-2 rounded-[50%]" />
        </div>
      </div>
    </div>
  </div>
</template>
