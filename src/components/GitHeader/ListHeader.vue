<script>
export default {
  data() {
    return {
      isMenuOpen: false
    }
  },
  methods: {
    toggleMenu() {
      this.isMenuOpen = !this.isMenuOpen
    }
  }
}
</script>

<template>
  <div class="">
    <div class="desktop hidden gap-4 md:flex">
      <a href="#" class="flex hover:bg-[#DDE3E8] p-[10px] rounded-lg">
        <img src="/src/assets/images/overview.svg" alt="" class="w-4 h-4 mt-[2px] mr-[3px]" />
        <p class="text-sm text-[#1F2329]">Overview</p>
      </a>
      <a href="#" class="flex hover:bg-[#DDE3E8] p-[10px] rounded-lg">
        <img src="/src/assets/images/repo.svg" alt="" class="w-4 h-4 mt-[2px] mr-[3px]" />
        <p class="text-sm text-[#1F2329]">Repositories</p>
      </a>
      <a href="#" class="flex hover:bg-[#DDE3E8] p-[10px] rounded-lg">
        <img src="/src/assets/images/overview.svg" alt="" class="w-4 h-4 mt-[2px] mr-[3px]" />
        <p class="text-sm text-[#1F2329]">Projects</p>
      </a>
      <a href="#" class="flex hover:bg-[#DDE3E8] p-[10px] rounded-lg">
        <img src="/src/assets/images/package.svg" alt="" class="w-4 h-4 mt-[2px] mr-[3px]" />
        <p class="text-sm text-[#1F2329]">Packages</p>
      </a>
      <a href="#" class="flex hover:bg-[#DDE3E8] p-[10px] rounded-lg">
        <img src="/src/assets/images/star.svg" alt="" class="w-4 h-4 mt-[2px] mr-[3px]" />
        <p class="text-sm text-[#1F2329]">Stars</p>
      </a>
    </div>

    <!-- Mobile View -->
    <div class="mobile flex justify-between md:hidden">
      <div>
        <a href="#" class="flex hover:bg-[#DDE3E8] p-[10px] rounded-lg">
          <img src="/src/assets/images/overview.svg" alt="" class="w-4 h-4 mt-[2px] mr-[3px]" />
          <p class="text-sm text-[#1F2329]">Overview</p>
        </a>
      </div>
      <div class="menu-container relative">
        <div class="menu">
          <img
            src="/src/assets/images/horizontal-menu.svg"
            alt=""
            class="w-5 h-5"
            @click="toggleMenu"
          />
        </div>
        <div class="menu-items bg-white z-20 p-2 rounded-md m-2" v-if="isMenuOpen">
          <a href="#" class="flex hover:bg-[#DDE3E8] p-[10px] rounded-lg">
            <img src="/src/assets/images/repo.svg" alt="" class="w-4 h-4 mt-[3px] mr-[3px]" />
            <p class="text-sm text-[#1F2329]">Repositories</p>
          </a>
          <a href="#" class="flex hover:bg-[#DDE3E8] p-[10px] rounded-lg">
            <img src="/src/assets/images/overview.svg" alt="" class="w-4 h-4 mt-[3px] mr-[3px]" />
            <p class="text-sm text-[#1F2329]">Projects</p>
          </a>
          <a href="#" class="flex hover:bg-[#DDE3E8] p-[10px] rounded-lg">
            <img src="/src/assets/images/package.svg" alt="" class="w-4 h-4 mt-[3px] mr-[3px]" />
            <p class="text-sm text-[#1F2329]">Packages</p>
          </a>
          <a href="#" class="flex hover:bg-[#DDE3E8] p-[10px] rounded-lg">
            <img src="/src/assets/images/star.svg" alt="" class="w-4 h-4 mt-[3px] mr-[3px]" />
            <p class="text-sm text-[#1F2329]">Stars</p>
          </a>
        </div>
      </div>
    </div>
  </div>
</template>
