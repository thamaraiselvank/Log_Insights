<template>
  <div class="q-pa-md" style="max-width: 300px">
    <div class="q-gutter-md">  
      
      <q-select standout="bg-teal text-white" v-model="optionsselected" :options="options" label=""  />

    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const model = ref(null);
const modelOptions = ref()

const options =  [
       'Error', 'Info', 'Warn', 'Fatal', 'Debug'
      ];
 let optionsselected = ref('Error')
//  let options2 =  [
//        'Error', 'Info', 'Warn', 'Fatal', 'Debug'
//       ];
</script>
