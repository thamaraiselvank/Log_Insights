<template>
  <div class="q-pa-md">
    <q-date
      v-model="date"
      today-btn
    />
  </div>
</template>

<script setup>
import { ref } from 'vue'


      let current = new Date();
    //  let date1 = `${current.getDate()}/${current.getMonth()+1}/${current.getFullYear()}`;
      
      let selecteddate = ref(`${current.getDate()}/${current.getMonth()+1}/${current.getFullYear()}`)
      let date = ref('selecteddate')
</script>