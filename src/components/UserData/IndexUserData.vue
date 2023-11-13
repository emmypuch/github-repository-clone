<template>
  <div class="mt-4 ml-2 md:ml-12">
    <div class="desktop hidden md:block">
      <div class="image mt-6 ml-6 md:relative">
        <a href="#">
          <img
            src="/src/assets/images/tihanapic.png"
            alt=""
            class="w-3/4 md:w-[260px] h-[240px] rounded-full md:rounded-[50%]"
          />
        </a>
      </div>
      <div
        class="avatar absolute left-[300px] top-[380px] bg-white z-10 rounded-[50%] border border-gray-300 p-2 h-8 w-8"
      >
        <img src="/src/assets/images/star.svg" alt="" class="w-4 h-4" />
      </div>
      <!-- Name -->
      <div class="userData">
        <div class="mt-4 ml-4">
          <h1 class="text-[1.7rem] text-[#1F2329]">Tihana Omowunmi</h1>
          <p class="text-[1.4rem] text-gray-500">tihana . she/her</p>
        </div>
      </div>
    </div>

    <!-- Mobile -->
    <div class="">
      <div class="mobile md:hidden flex">
        <div class="image mt-6 ml-6 md:hidden">
          <a href="#">
            <img
              src="/src/assets/images/tihanapic.png"
              alt=""
              class="w-[60px] h-[60px] rounded-[50%]"
            />
          </a>
        </div>
        <!-- Name -->
        <div class="userData">
          <div class="mt-6 ml-4">
            <h1 class="text-[1.4rem] text-[#1F2329]">Tihana Omowunmi</h1>
            <p class="text-[1.1rem] text-gray-500">tihana . she/her</p>
          </div>
        </div>
      </div>
      <div
        class="md:hidden flex ml-4 mt-4 gap-[3px] border border-gray-400 rounded-lg px-[15px] text-center py-[6px]"
      >
        <div>👩‍💻</div>
        <div class="text-[0.8rem] text-center text-[#1F2329] ml-2 mt-1">Always learning</div>
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
    <div class="follow-container flex mt-4 ml-4 gap-1">
      <div class="follower flex">
        <img src="/src/assets/images/users.svg" alt="" class="w-4 h-4 mt-1" />
        <h6 class="ml-1 text-[1rem] text-gray-500">
          <span class="text-[#1F2329]">7</span> followers
        </h6>
      </div>
      <span>.</span>
      <div class="follower flex">
        <h6 class="ml-1 text-[1rem] text-gray-500">
          <span class="text-[#1F2329]">30</span> following
        </h6>
      </div>
    </div>

    <!-- Links -->
    <div class="link-container mt-4 ml-4">
      <ul>
        <li class="flex gap-1">
          <img src="/src/assets/images/office.svg" alt="" class="w-4 h-4 mt-[3px]" />
          <p class="text-[#1F2329] text-base">Patricia Technologies</p>
        </li>
        <li class="flex gap-1 mt-1">
          <img src="/src/assets/images/map.svg" alt="" class="w-4 h-4 mt-[3px]" />
          <p class="text-[#1F2329] text-base">Lagos, Nigeria</p>
        </li>
        <li class="flex gap-1 mt-1">
          <img src="/src/assets/images/email.svg" alt="" class="w-4 h-4 mt-[3px]" />
          <a href="mailto:wunmiadesuyi@gmail.com" class="text-[#1F2329] text-base"
            >tihana@gmail.com</a
          >
        </li>
        <li class="flex gap-1 mt-1">
          <img src="/src/assets/images/link.svg" alt="" class="w-4 h-4 mt-[3px]" />
          <a href="#" target="_blank" class="text-[#1F2329] text-base">https://tihana.com</a>
        </li>
        <li class="flex gap-1 mt-1">
          <img src="/src/assets/images/office.svg" alt="" class="w-4 h-4 mt-[3px]" />
          <a href="#" target="_blank" class="text-[#1F2329] text-base">twitter.com</a>
        </li>
      </ul>
    </div>
    <div class="bg-gray-200 w-[100%] md:w-[70%] h-[1px] mt-3 ml-4"></div>

    <!-- Achievements -->
    <div class="achievement-container ml-4 mt-4">
      <h3 class="text-[#1F2329] text-lg">Acchievements</h3>
      <div class="flex gap-2 mt-2">
        <div>
          <a href="#">
            <img src="/src/assets/images/starstruck.png" alt="" class="w-16 h-16" />
          </a>
        </div>
        <div>
          <a href="#">
            <img src="/src/assets/images/pullshark.png" alt="" class="w-16 h-16" />
          </a>
        </div>
        <div>
          <a href="#">
            <img src="/src/assets/images/arcticcode.png" alt="" class="w-16 h-16" />
          </a>
        </div>
      </div>
      <div class="btn flex gap-1 mt-3">
        <div class="flex gap-2">
          <div
            class="text-[#1E7F39] text-[12px] text-center border border-[#1E7F39] py-[0.12rem] px-[0.5rem] rounded-[2rem]"
          >
            Beta
          </div>
          <div>
            <a href="#" class="text-[#0D68D9] text-[13px] hover:underline">Send feedback</a>
          </div>
        </div>
      </div>
    </div>
    <div class="bg-gray-200 w-[100%] md:w-[70%] h-[1px] mt-3 ml-4"></div>

    <!-- Organization -->
    <div class="organization-container ml-4 mt-4 pb-4">
      <h3 class="text-[#1F2329] text-lg">Oragnizations</h3>
      <div class="flex gap-[3px] mt-2">
        <div>
          <a href="#" class="">
            <img
              src="/src/assets/images/saraloge.jpeg"
              alt=""
              class="w-10 h-10 bg-transparent px-1 py-2 border border-gray-400 rounded-lg"
            />
          </a>
        </div>
        <div>
          <a href="#" class="">
            <img
              src="/src/assets/images/logo.png"
              alt=""
              class="w-10 h-10 bg-transparent px-1 py-2 border border-gray-400 rounded-lg"
            />
          </a>
        </div>
        <div>
          <a href="#">
            <img
              src="/src/assets/images/regal.jpeg"
              alt=""
              class="w-10 h-10 bg-transparent px-1 py-2 border border-gray-400 rounded-lg"
            />
          </a>
        </div>
      </div>
    </div>
  </div>
</template>
