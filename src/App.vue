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

  <main class="flex flex-col md:grid md:grid-cols-2 gap-2">
    <div>
      <IndexUserData class="p-0 md:p-6" />
    </div>
    <div>
      <IndexRepo />
    </div>
  </main>
</template>
