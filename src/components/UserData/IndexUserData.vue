<template>
  <div class="mt-4 ml-12">
    <div>
      <div class="image mt-6 relative">
        <a href="#">
          <img
            src="/src/assets/images/tihanapic.png"
            alt=""
            class="w-[260px] h-[260px] relative rounded-[50%]"
          />
        </a>
      </div>
      <div
        class="avatar absolute left-[280px] top-[360px] bg-white z-10 rounded-[50%] border border-gray-300 p-2 h-8 w-8"
      >
        <img src="/src/assets/images/star.svg" alt="" class="w-4 h-4" />
      </div>
    </div>

    <!-- Name -->
    <div class="userData">
      <div class="mt-4 ml-4">
        <h1 class="text-[1.7rem]">Tihana Omowunmi</h1>
        <p class="text-[1.4rem] text-gray-500">tihana . she/her</p>
      </div>
    </div>

    <!-- Bio -->
    <div class="bio mt-3 ml-4">
      <h6 class="text-base">Frontend Engineer | 🐶 Mum | Vue | Ice-Cream ❤️</h6>
      <div class="btn mt-3 max-w-full">
        <button
          class="edit bg-[#f3f4f7] px-[5px] py-[8px] text-center md:w-[80%] w-[100%] border text-base border-gray-300 rounded-lg"
        >
          Edit profile
        </button>
      </div>
    </div>
  </div>
</template>
