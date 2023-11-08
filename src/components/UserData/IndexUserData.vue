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
        <h1 class="text-[1.7rem] text-[#1F2329]">Tihana Omowunmi</h1>
        <p class="text-[1.4rem] text-gray-500">tihana . she/her</p>
      </div>
    </div>

    <!-- Bio -->
    <div class="bio mt-3 ml-4">
      <h6 class="text-base text-[#1F2329]">Frontend Engineer | 🐶 Mum | Vue | Ice-Cream ❤️</h6>
      <div class="btn mt-3 max-w-full">
        <button
          class="edit bg-[#f3f4f7] text-[#1F2329] hover:bg-[#e8ebee] px-[5px] py-[8px] text-center md:w-[80%] w-[100%] border text-base border-gray-300 rounded-lg"
        >
          Edit profile
        </button>
      </div>
    </div>

    <!-- Follows -->
    <div class="follow-container flex mt-4 ml-4 gap-2">
      <div class="follower flex">
        <img src="/src/assets/images/users.svg" alt="" class="w-4 h-4 mt-1" />
        <h6 class="ml-1 text-[1rem] text-gray-500">
          <span class="text-[#1F2329]">7</span> followers
        </h6>
      </div>
      <div class="follower flex">
        <h6 class="ml-1 text-[1rem] text-gray-500">
          <span class="text-[#1F2329]">30</span> following
        </h6>
      </div>
    </div>
  </div>
</template>
