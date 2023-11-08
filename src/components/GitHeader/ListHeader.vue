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
      <div class="flex">
        <img src="/src/assets/images/overview.svg" alt="" class="w-4 h-4 mt-[2px] mr-[3px]" />
        <p class="text-sm">Overview</p>
      </div>
      <div class="flex">
        <img src="/src/assets/images/repo.svg" alt="" class="w-4 h-4 mt-[2px] mr-[3px]" />
        <p class="text-sm">Repositories</p>
      </div>
      <div class="flex">
        <img src="/src/assets/images/overview.svg" alt="" class="w-4 h-4 mt-[2px] mr-[3px]" />
        <p class="text-sm">Projects</p>
      </div>
      <div class="flex">
        <img src="/src/assets/images/package.svg" alt="" class="w-4 h-4 mt-[2px] mr-[3px]" />
        <p class="text-sm">Packages</p>
      </div>
      <div class="flex">
        <img src="/src/assets/images/star.svg" alt="" class="w-4 h-4 mt-[2px] mr-[3px]" />
        <p class="text-sm">Stars</p>
      </div>
    </div>

    <!-- Mobile View -->
    <div class="mobile flex justify-between md:hidden">
      <div>
        <div class="flex">
          <img src="/src/assets/images/overview.svg" alt="" class="w-4 h-4 mt-[2px] mr-[3px]" />
          <p class="text-sm">Overview</p>
        </div>
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
        <div class="menu-items bg-red-500 p-2 rounded-md m-2" v-if="isMenuOpen">
          <div class="flex m-1">
            <img src="/src/assets/images/repo.svg" alt="" class="w-4 h-4 mt-[3px] mr-[3px]" />
            <p class="text-sm">Repositories</p>
          </div>
          <div class="flex m-1">
            <img src="/src/assets/images/overview.svg" alt="" class="w-4 h-4 mt-[3px] mr-[3px]" />
            <p class="text-sm">Projects</p>
          </div>
          <div class="flex m-1">
            <img src="/src/assets/images/package.svg" alt="" class="w-4 h-4 mt-[3px] mr-[3px]" />
            <p class="text-sm">Packages</p>
          </div>
          <div class="flex m-1">
            <img src="/src/assets/images/star.svg" alt="" class="w-4 h-4 mt-[3px] mr-[3px]" />
            <p class="text-sm">Stars</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
