<script setup>
import IndexHeader from './components/GitHeader/IndexHeader.vue'
import IndexRepo from './components/Repositories/IndexRepo.vue'
import IndexUserData from './components/UserData/IndexUserData.vue'
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
    </div>
  </main>
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
