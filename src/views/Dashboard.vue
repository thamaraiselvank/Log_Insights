<template>
    <div class="q-mt-md q-mr-sm">
      <q-toolbar class="bg-purple text-white shadow-2 rounded-borders">
   <!-- <q-btn flat label="Log Insights" /> -->  
  
        <!--
          notice shrink property since we are placing it
          as child of QToolbar
        -->
        <q-tabs v-model="tab" shrink>
          <q-tab name="Insights" label="Insights"/>
          <q-tab name="Dashboard" label="Dashboard" />
          <q-tab name="Device" label="Device" />
          <q-tab name="Logs and Reports" label="Logs and Reports" />
        </q-tabs>
      </q-toolbar>
    </div>
  </template>
  
  <script>
  import { ref } from 'vue'
  
  export default {
    setup () {
      return {
        tab: ref('')
      }
    }
  }
  </script>
  