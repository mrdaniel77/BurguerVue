<template>
  <div class="col-12 col-sm-6 col-md-4 col-lg-3 mt-2">
    <div class="card d-flex justify-content-center align-items-center">
      <div class="card-body text-center">
        <h5 class="card-title">{{message}}</h5>
        <div class="row justify-content-center">
          <div class="col">
            <button @click="reverse" class="btn btn-primary ">Reverta a mensagem</button>
          </div>
          <div class="col">
            <button @click="notify" class="btn btn-info ">Notificação do texto</button>
          </div>
        </div>
      </div>
    </div>
  </div>
  <div class="col-12 col-sm-6 col-md-4 col-lg-3 mt-2">
    <div class="card d-flex justify-content-center align-items-center">
      <div class="card-body text-center">
        <h5 class="card-title">A contagem é {{number}}</h5>      
        <div class="row justify-content-center">
          <div class="col">
            <button @click="adicionar" class="btn btn-success">Somar</button>
          </div>
          <div class="col">
            <button @click="retirar" class="btn btn-danger">Subtrair</button>
          </div>
        </div> 
      </div>
    </div> 
  </div>
  <div class="col-12 col-sm-6 col-md-4 col-lg-3 mt-2">
    <div class="card text-center">
      <div class="card-body">
        <h5 class="card-title">Lista {{ list }}</h5>
        <div class="card-text">
          <div class="d-flex justify-content-center gap-2">
            <button @click="list.push(list.length + 1)" class="btn btn-success">Adicionar</button>
            <button @click="list.pop()" class="btn btn-danger">Tirar</button>
            <button @click="list.reverse()" class="btn btn-primary">Inverter</button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>

import { ref } from 'vue';

  let message = ref('Olá, seja muito bem vindo !');
  let number = ref(0);
  let list = ref([1,2,3,4,5]);

  function reverse(){
    message.value = message.value.split('').reverse().join('');
  }

  function notify(){
    alert(message.value);
  }

  function adicionar(){
    number.value++
  }
  function retirar(){
    number.value--
  }

</script>

<style scoped>

</style>
