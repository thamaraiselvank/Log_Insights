<template>
    <div class="q-pa-md">
      <q-btn color="teal" label="Open Dialog" @click="dialog = true" />
  
      <q-dialog v-model="dialog">
        <q-layout view="lhh LpR lff" container style="height: 500px" class="shadow-2" :class="$q.dark.isActive ? 'bg-grey-9' : 'bg-grey-3'">
          
  
          <q-page-container>
       <q-page class="q-pa-md">
        <router-view name="Date"></router-view>
        <Date/>
       </q-page>

          </q-page-container>
        </q-layout>
      </q-dialog>
    </div>
  </template>
  
  <script>
  import { ref } from 'vue'
  import Date from './Date.vue';
  
  export default {
    components:{
        Date
    },
    setup () {
      return {
        dialog: ref(false),
        
       
      }
    }
  }
  </script>
  