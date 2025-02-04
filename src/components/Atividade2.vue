<template>
  <div class="col-12 col-sm-6 col-md-4 col-lg-3 mt-2">
    <div class="card d-flex justify-content-center align-items-center">
      <div class="card-body text-center">
          <h5 class="card-title" >Edite-me : {{text}}</h5>
          <input type="text" class="form-control" v-model="text">            
      </div>
    </div>
  </div>
  <div class="col-12 col-sm-6 col-md-4 col-lg-3 mt-2">
    <div class="card d-flex justify-content-center align-items-center">
      <div class="card-body ">
      <form id="search">          
        <div class="mb-3">
          <label for="Search" class="form-label">Search</label>
          <input type="query" class="form-control" v-model="searchQuery">
        </div>
      </form>
      <DemoGrid
        :data="gridData"
        :columns="gridColumns"
        :filter-key="searchQuery">
      </DemoGrid>
      </div>
    </div>
  </div>
</template>

<script setup>

import DemoGrid from './Grid.vue'
import { ref } from 'vue'

const searchQuery = ref('')
const gridColumns = ['name', 'power']
const gridData = [
  { name: 'Daniel', power: Infinity },
  { name: 'Wesley', power: 9000 },
  { name: 'Vitor', power: 7000 },
  { name: 'Leo', power: 8000 },
  { name: 'Leandro', power: 8500 }
]
  let text = ref('Texto');
 
</script>
