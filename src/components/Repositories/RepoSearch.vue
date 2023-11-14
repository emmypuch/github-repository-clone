<script>
export default {
  data() {
    return {
      isStarred: false,
      isHovered: false
      // isDropdownOpen: false,
      // checklist: ['Item 1', 'Item 2']
    }
  },
  methods: {
    toggleStar() {
      this.isStarred = !this.isStarred
    }
  }
}
</script>

<template>
  <div>
    <div class="hidden md:flex">
      <div class="input w-full mr-6">
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
            <p class="text-[#1f2329] text-[0.9rem]">Sort</p>
            <img src="/src/assets/images/chevron-down.svg" alt="" class="w-3 h-3 mt-[5px]" />
          </a>
        </div>
        <div>
          <a href="#" class="flex gap-[3px] bg-[#1E883E] px-[15px] text-center py-[6px] rounded-lg">
            <img src="/src/assets/images/rep.svg" alt="" class="w-3 h-3 mt-[1px]" />
            <p class="text-[#f2f7f3] text-[0.9rem]">New</p>
          </a>
        </div>
      </div>
    </div>
    <div class="bg-gray-200 w-[100%] md:w-[100%] h-[1px] mt-3 ml-2"></div>

    <!-- Mobile view -->
    <div class="flex-col md:hidden ml-2 mr-0">
      <div>
        <a href="#" class="flex gap-[3px] bg-[#1E883E] px-[15px] text-center py-[6px] rounded-lg">
          <img src="/src/assets/images/rep.svg" alt="" class="w-3 h-3 mt-[1px]" />
          <p class="text-[#f2f7f3] text-[0.9rem]">New</p>
        </a>
      </div>
      <div class="input w-full mr-6 mt-6">
        <input
          type="text"
          placeholder="Find a repository..."
          class="rounded-lg border border-gray-400 text-[0.9rem] text-gray-500 px-[15px] py-[5px] w-full"
        />
      </div>
      <div class="flex gap-2 mt-2">
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
            <p class="text-[#1f2329] text-[0.9rem]">Sort</p>
            <img src="/src/assets/images/chevron-down.svg" alt="" class="w-3 h-3 mt-[5px]" />
          </a>
        </div>
      </div>
    </div>
    <div class="bg-gray-200 w-[100%] md:w-[100%] h-[1px] mt-3 ml-2"></div>

    <!-- Repositories -->
    <div class="ml-2 mt-8">
      <div class="desktop hidden md:flex md:justify-between">
        <div class="repo-name flex gap-2">
          <div>
            <a href="#" class="text-[#0869DA] text-[1rem] hover:underline">JavaScript Calculator</a>
          </div>
          <div class="flex items-center mb-[10px]">
            <div class="border border-gray-400 py-[0.12rem] px-[0.5rem] rounded-[2rem]">
              <p class="text-[#1F2329] text-[12px] text-center">Public</p>
            </div>
          </div>
        </div>
        <div class="flex">
          <div @click="toggleStar">
            <a
              href="#"
              class="flex gap-[2px] bg-gray-100 border border-gray-400 px-[8px] text-center py-[6px] rounded-lg"
            >
              <img
                :src="
                  isStarred ? '/src/assets/images/star-yellow.svg' : '/src/assets/images/star.svg'
                "
                alt=""
                class="w-5 h-5"
              />
              <p :class="{ 'text-[#1f2329]': isStarred, 'text-[#1f2329]': !isStarred }">
                {{ isStarred ? 'Starred' : 'Star' }}
              </p>
              <div @click="toggleDropdown" class="relative right-[3px] text-center">
                <img
                  src="/src/assets/images/chevron-down.svg"
                  alt=""
                  class="w-3 h-3 mt-[7px] ml-4"
                />
              </div>
            </a>
          </div>
        </div>
      </div>

      <!-- Mobile -->
      <div class="md:hidden">
        <div>
          <a href="#" class="text-[#0869DA] text-[1rem] hover:underline">JavaScript Calculator</a>
        </div>
        <div class="repo-name flex justify-between gap-3 mt-3">
          <div class="flex items-center mb-[10px]">
            <div class="border border-gray-400 py-[0.12rem] px-[0.5rem] rounded-[2rem]">
              <p class="text-[#1F2329] text-[12px] text-center">Public</p>
            </div>
          </div>
          <div class="">
            <a
              href="#"
              class="flex gap-[3px] bg-gray-100 border border-gray-400 px-[25px] text-center py-[6px] rounded-lg"
            >
              <img src="/src/assets/images/star.svg" alt="" class="w-5 h-5" />
              <p class="text-[#1f2329] text-[0.9rem] ml-2">Star</p>
              <img src="/src/assets/images/chevron-down.svg" alt="" class="w-3 h-3 mt-[5px] ml-2" />
            </a>
          </div>
        </div>
      </div>
      <!-- Language -->
      <div class="flex justify-between ml-2 mt-4">
        <div class="flex gap-2">
          <div class="flex gap-[3px]">
            <div class="rounded-[50%] bg-[#41B883] h-3 w-3 mt-[3px]"></div>
            <div class="text-[0.7rem] text-[#666D76]">Vue</div>
          </div>
          <div class="text-[0.7rem] text-[#666D76]">Updated yesterday</div>
        </div>

        <div
          class="line relative cursor-pointer bg-[#AAE9B6] h-[2px] w-[130px]"
          @mouseover="isHovered = true"
          @mouseleave="isHovered = false"
        ></div>
        <div
          class="text absolute text-center right-[0%] bg-black text-white w-[150px] p-[3px] rounded-lg text-[12px]"
        >
          Past year of activity
        </div>
      </div>
    </div>
    <div class="bg-gray-200 w-[100%] md:w-[100%] h-[1px] mt-4 ml-2"></div>

    <!-- Repository2 -->
    <div class="ml-2 mt-8">
      <div class="desktop hidden md:flex md:justify-between">
        <div class="repo-name flex gap-2">
          <div>
            <a href="#" class="text-[#0869DA] text-[1rem] hover:underline">JavaScript Calculator</a>
          </div>
          <div class="flex items-center mb-[10px]">
            <div class="border border-gray-400 py-[0.12rem] px-[0.5rem] rounded-[2rem]">
              <p class="text-[#1F2329] text-[12px] text-center">Public</p>
            </div>
          </div>
        </div>
        <div>
          <a
            href="#"
            class="flex gap-[2px] bg-gray-100 border border-gray-400 px-[8px] text-center py-[6px] rounded-lg"
          >
            <img src="/src/assets/images/star.svg" alt="" class="w-5 h-5" />
            <p class="text-[#1f2329] text-[0.9rem] ml-1">Star</p>
            <img src="/src/assets/images/chevron-down.svg" alt="" class="w-3 h-3 mt-[5px] ml-2" />
          </a>
        </div>
      </div>

      <!-- Mobile -->
      <div class="md:hidden">
        <div>
          <a href="#" class="text-[#0869DA] text-[1rem] hover:underline">JavaScript Calculator</a>
        </div>
        <div class="repo-name flex justify-between gap-3 mt-3">
          <div class="flex items-center mb-[10px]">
            <div class="border border-gray-400 py-[0.12rem] px-[0.5rem] rounded-[2rem]">
              <p class="text-[#1F2329] text-[12px] text-center">Public</p>
            </div>
          </div>
          <div class="">
            <a
              href="#"
              class="flex gap-[3px] bg-gray-100 border border-gray-400 px-[25px] text-center py-[6px] rounded-lg"
            >
              <img src="/src/assets/images/star.svg" alt="" class="w-5 h-5" />
              <p class="text-[#1f2329] text-[0.9rem] ml-2">Star</p>
              <img src="/src/assets/images/chevron-down.svg" alt="" class="w-3 h-3 mt-[5px] ml-2" />
            </a>
          </div>
        </div>
      </div>
      <!-- Language -->
      <div class="flex justify-between ml-2 mt-4">
        <div class="flex gap-2">
          <div class="flex gap-[3px]">
            <div class="rounded-[50%] bg-[#41B883] h-3 w-3 mt-[3px]"></div>
            <div class="text-[0.7rem] text-[#666D76]">Vue</div>
          </div>
          <div class="text-[0.7rem] text-[#666D76]">Updated yesterday</div>
        </div>

        <div
          class="line relative cursor-pointer bg-[#AAE9B6] h-[2px] w-[130px]"
          @mouseover="isHovered = true"
          @mouseleave="isHovered = false"
        ></div>
        <div
          class="text absolute text-center right-[0%] bg-black text-white w-[150px] p-[3px] rounded-lg text-[12px]"
        >
          Past year of activity
        </div>
      </div>
    </div>
    <div class="bg-gray-200 w-[100%] md:w-[100%] h-[1px] mt-4 ml-2"></div>

    <!-- Repository3 -->
    <div class="ml-2 mt-8">
      <div class="desktop hidden md:flex md:justify-between">
        <div class="repo-name flex gap-2">
          <div>
            <a href="#" class="text-[#0869DA] text-[1rem] hover:underline">JavaScript Calculator</a>
          </div>
          <div class="flex items-center mb-[10px]">
            <div class="border border-gray-400 py-[0.12rem] px-[0.5rem] rounded-[2rem]">
              <p class="text-[#1F2329] text-[12px] text-center">Public</p>
            </div>
          </div>
        </div>
        <div>
          <a
            href="#"
            class="flex gap-[2px] bg-gray-100 border border-gray-400 px-[8px] text-center py-[6px] rounded-lg"
          >
            <img src="/src/assets/images/star.svg" alt="" class="w-5 h-5" />
            <p class="text-[#1f2329] text-[0.9rem] ml-1">Star</p>
            <img src="/src/assets/images/chevron-down.svg" alt="" class="w-3 h-3 mt-[5px] ml-2" />
          </a>
        </div>
      </div>

      <!-- Mobile -->
      <div class="md:hidden">
        <div>
          <a href="#" class="text-[#0869DA] text-[1rem] hover:underline">JavaScript Calculator</a>
        </div>
        <div class="repo-name flex justify-between gap-3 mt-3">
          <div class="flex items-center mb-[10px]">
            <div class="border border-gray-400 py-[0.12rem] px-[0.5rem] rounded-[2rem]">
              <p class="text-[#1F2329] text-[12px] text-center">Public</p>
            </div>
          </div>
          <div class="">
            <a
              href="#"
              class="flex gap-[3px] bg-gray-100 border border-gray-400 px-[25px] text-center py-[6px] rounded-lg"
            >
              <img src="/src/assets/images/star.svg" alt="" class="w-5 h-5" />
              <p class="text-[#1f2329] text-[0.9rem] ml-2">Star</p>
              <img src="/src/assets/images/chevron-down.svg" alt="" class="w-3 h-3 mt-[5px] ml-2" />
            </a>
          </div>
        </div>
      </div>
      <!-- Language -->
      <div class="flex justify-between ml-2 mt-4">
        <div class="flex gap-2">
          <div class="flex gap-[3px]">
            <div class="rounded-[50%] bg-[#41B883] h-3 w-3 mt-[3px]"></div>
            <div class="text-[0.7rem] text-[#666D76]">Vue</div>
          </div>
          <div class="text-[0.7rem] text-[#666D76]">Updated yesterday</div>
        </div>

        <div
          class="line relative cursor-pointer bg-[#AAE9B6] h-[2px] w-[130px]"
          @mouseover="isHovered = true"
          @mouseleave="isHovered = false"
        ></div>
        <div
          class="text absolute text-center right-[0%] bg-black text-white w-[150px] p-[3px] rounded-lg text-[12px]"
        >
          Past year of activity
        </div>
      </div>
    </div>
    <div class="bg-gray-200 w-[100%] md:w-[100%] h-[1px] mt-4 ml-2"></div>

    <!-- Repository4 -->
    <div class="ml-2 mt-8">
      <div class="desktop hidden md:flex md:justify-between">
        <div class="repo-name flex gap-2">
          <div>
            <a href="#" class="text-[#0869DA] text-[1rem] hover:underline">JavaScript Calculator</a>
          </div>
          <div class="flex items-center mb-[10px]">
            <div class="border border-gray-400 py-[0.12rem] px-[0.5rem] rounded-[2rem]">
              <p class="text-[#1F2329] text-[12px] text-center">Public</p>
            </div>
          </div>
        </div>
        <div>
          <a
            href="#"
            class="flex gap-[2px] bg-gray-100 border border-gray-400 px-[8px] text-center py-[6px] rounded-lg"
          >
            <img src="/src/assets/images/star.svg" alt="" class="w-5 h-5" />
            <p class="text-[#1f2329] text-[0.9rem] ml-1">Star</p>
            <img src="/src/assets/images/chevron-down.svg" alt="" class="w-3 h-3 mt-[5px] ml-2" />
          </a>
        </div>
      </div>

      <!-- Mobile -->
      <div class="md:hidden">
        <div>
          <a href="#" class="text-[#0869DA] text-[1rem] hover:underline">JavaScript Calculator</a>
        </div>
        <div class="repo-name flex justify-between gap-3 mt-3">
          <div class="flex items-center mb-[10px]">
            <div class="border border-gray-400 py-[0.12rem] px-[0.5rem] rounded-[2rem]">
              <p class="text-[#1F2329] text-[12px] text-center">Public</p>
            </div>
          </div>
          <div class="">
            <a
              href="#"
              class="flex gap-[3px] bg-gray-100 border border-gray-400 px-[25px] text-center py-[6px] rounded-lg"
            >
              <img src="/src/assets/images/star.svg" alt="" class="w-5 h-5" />
              <p class="text-[#1f2329] text-[0.9rem] ml-2">Star</p>
              <img src="/src/assets/images/chevron-down.svg" alt="" class="w-3 h-3 mt-[5px] ml-2" />
            </a>
          </div>
        </div>
      </div>
      <!-- Language -->
      <div class="flex justify-between ml-2 mt-4">
        <div class="flex gap-2">
          <div class="flex gap-[3px]">
            <div class="rounded-[50%] bg-[#41B883] h-3 w-3 mt-[3px]"></div>
            <div class="text-[0.7rem] text-[#666D76]">Vue</div>
          </div>
          <div class="text-[0.7rem] text-[#666D76]">Updated yesterday</div>
        </div>

        <div
          class="line relative cursor-pointer bg-[#AAE9B6] h-[2px] w-[130px]"
          @mouseover="isHovered = true"
          @mouseleave="isHovered = false"
        ></div>
        <div
          class="text absolute text-center right-[0%] bg-black text-white w-[150px] p-[3px] rounded-lg text-[12px]"
        >
          Past year of activity
        </div>
      </div>
    </div>
    <div class="bg-gray-200 w-[100%] md:w-[100%] h-[1px] mt-4 ml-2"></div>

    <!-- Repository5 -->
    <div class="ml-2 mt-8">
      <div class="desktop hidden md:flex md:justify-between">
        <div class="repo-name flex gap-2">
          <div>
            <a href="#" class="text-[#0869DA] text-[1rem] hover:underline">JavaScript Calculator</a>
          </div>
          <div class="flex items-center mb-[10px]">
            <div class="border border-gray-400 py-[0.12rem] px-[0.5rem] rounded-[2rem]">
              <p class="text-[#1F2329] text-[12px] text-center">Public</p>
            </div>
          </div>
        </div>
        <div>
          <a
            href="#"
            class="flex gap-[2px] bg-gray-100 border border-gray-400 px-[8px] text-center py-[6px] rounded-lg"
          >
            <img src="/src/assets/images/star.svg" alt="" class="w-5 h-5" />
            <p class="text-[#1f2329] text-[0.9rem] ml-1">Star</p>
            <img src="/src/assets/images/chevron-down.svg" alt="" class="w-3 h-3 mt-[5px] ml-2" />
          </a>
        </div>
      </div>

      <!-- Mobile -->
      <div class="md:hidden">
        <div>
          <a href="#" class="text-[#0869DA] text-[1rem] hover:underline">JavaScript Calculator</a>
        </div>
        <div class="repo-name flex justify-between gap-3 mt-3">
          <div class="flex items-center mb-[10px]">
            <div class="border border-gray-400 py-[0.12rem] px-[0.5rem] rounded-[2rem]">
              <p class="text-[#1F2329] text-[12px] text-center">Public</p>
            </div>
          </div>
          <div class="">
            <a
              href="#"
              class="flex gap-[3px] bg-gray-100 border border-gray-400 px-[25px] text-center py-[6px] rounded-lg"
            >
              <img src="/src/assets/images/star.svg" alt="" class="w-5 h-5" />
              <p class="text-[#1f2329] text-[0.9rem] ml-2">Star</p>
              <img src="/src/assets/images/chevron-down.svg" alt="" class="w-3 h-3 mt-[5px] ml-2" />
            </a>
          </div>
        </div>
      </div>
      <!-- Language -->
      <div class="flex justify-between ml-2 mt-4">
        <div class="flex gap-2">
          <div class="flex gap-[3px]">
            <div class="rounded-[50%] bg-[#41B883] h-3 w-3 mt-[3px]"></div>
            <div class="text-[0.7rem] text-[#666D76]">Vue</div>
          </div>
          <div class="text-[0.7rem] text-[#666D76]">Updated yesterday</div>
        </div>

        <div
          class="line relative cursor-pointer bg-[#AAE9B6] h-[2px] w-[130px]"
          @mouseover="isHovered = true"
          @mouseleave="isHovered = false"
        ></div>
        <div
          class="text absolute text-center right-[0%] bg-black text-white w-[150px] p-[3px] rounded-lg text-[12px]"
        >
          Past year of activity
        </div>
      </div>
    </div>
    <div class="bg-gray-200 w-[100%] md:w-[100%] h-[1px] mt-4 ml-2"></div>

    <!-- Repository6 -->
    <div class="ml-2 mt-8">
      <div class="desktop hidden md:flex md:justify-between">
        <div class="repo-name flex gap-2">
          <div>
            <a href="#" class="text-[#0869DA] text-[1rem] hover:underline">JavaScript Calculator</a>
          </div>
          <div class="flex items-center mb-[10px]">
            <div class="border border-gray-400 py-[0.12rem] px-[0.5rem] rounded-[2rem]">
              <p class="text-[#1F2329] text-[12px] text-center">Public</p>
            </div>
          </div>
        </div>
        <div>
          <a
            href="#"
            class="flex gap-[2px] bg-gray-100 border border-gray-400 px-[8px] text-center py-[6px] rounded-lg"
          >
            <img src="/src/assets/images/star.svg" alt="" class="w-5 h-5" />
            <p class="text-[#1f2329] text-[0.9rem] ml-1">Star</p>
            <img src="/src/assets/images/chevron-down.svg" alt="" class="w-3 h-3 mt-[5px] ml-2" />
          </a>
        </div>
      </div>

      <!-- Mobile -->
      <div class="md:hidden">
        <div>
          <a href="#" class="text-[#0869DA] text-[1rem] hover:underline">JavaScript Calculator</a>
        </div>
        <div class="repo-name flex justify-between gap-3 mt-3">
          <div class="flex items-center mb-[10px]">
            <div class="border border-gray-400 py-[0.12rem] px-[0.5rem] rounded-[2rem]">
              <p class="text-[#1F2329] text-[12px] text-center">Public</p>
            </div>
          </div>
          <div class="">
            <a
              href="#"
              class="flex gap-[3px] bg-gray-100 border border-gray-400 px-[25px] text-center py-[6px] rounded-lg"
            >
              <img src="/src/assets/images/star.svg" alt="" class="w-5 h-5" />
              <p class="text-[#1f2329] text-[0.9rem] ml-2">Star</p>
              <img src="/src/assets/images/chevron-down.svg" alt="" class="w-3 h-3 mt-[5px] ml-2" />
            </a>
          </div>
        </div>
      </div>
      <!-- Language -->
      <div class="flex justify-between ml-2 mt-4">
        <div class="flex gap-2">
          <div class="flex gap-[3px]">
            <div class="rounded-[50%] bg-[#41B883] h-3 w-3 mt-[3px]"></div>
            <div class="text-[0.7rem] text-[#666D76]">Vue</div>
          </div>
          <div class="text-[0.7rem] text-[#666D76]">Updated yesterday</div>
        </div>

        <div
          class="line relative cursor-pointer bg-[#AAE9B6] h-[2px] w-[130px]"
          @mouseover="isHovered = true"
          @mouseleave="isHovered = false"
        ></div>
        <div
          class="text absolute text-center bottom-[-21%] right-[0%] bg-black text-white w-[150px] p-[3px] rounded-lg text-[12px]"
        >
          Past year of activity
        </div>
      </div>
    </div>
    <div class="bg-gray-200 w-[100%] md:w-[100%] h-[1px] mt-4 ml-2"></div>
  </div>
</template>

<style>
.text {
  transform: translateX(-50%);
  display: none;
}

.line:hover + .text {
  display: block;
}
</style>
