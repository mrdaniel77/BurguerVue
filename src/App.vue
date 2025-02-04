<script setup>

  import Atividade from './components/Atividade.vue'
  import Atividade2 from './components/Atividade2.vue'
  import Navbar from './components/Navbar.vue'
  
</script>

<template>
  <div class="container-fluid">
    <header class="">
      <Navbar />
    </header>

    <main class="mt-4">
      <div class="row justify-content-center">       
        <Atividade />
        <Atividade2 />
      </div>
    </main>

  </div>

</template>






