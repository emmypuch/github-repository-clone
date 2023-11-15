<script setup>
import IndexHeader from './components/GitHeader/IndexHeader.vue'
import IndexRepo from './components/Repositories/IndexRepo.vue'
import IndexPrev from './components/Pagination/IndexPrev.vue'
import IndexNext from './components/Pagination/IndexNext.vue'
import IndexUserData from './components/UserData/IndexUserData.vue'
import GitFooter from './components/GitFooter.vue'
</script>

<template>
  <header>
    <IndexHeader />
    <div class="wrapper"></div>
  </header>

  <main class="">
    <div>
      <IndexUserData class="p-0 md:p-6" />
    </div>
    <div>
      <IndexRepo />
      <div class="flex justify-center items-center gap-4 mt-10">
        <div>
          <IndexPrev />
        </div>
        <div>
          <IndexNext />
        </div>
      </div>
    </div>
  </main>
  <div class="mt-4 ml-4 md:ml-20 bg-gray-200 w-[100%] md:w-[90%] h-[1px]"></div>
  <footer>
    <GitFooter />
  </footer>
</template>

<style>
main {
  display: grid;
  grid-template-columns: 30% 70%;
  gap: 20px;
}

@media screen and (max-width: 768px) {
  main {
    display: flex;
    flex-direction: column;
  }
}
</style>
