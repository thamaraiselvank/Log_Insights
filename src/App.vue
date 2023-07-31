<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated class="glossy">
      
    </q-header>
    <q-page-container>
      <Dashboard />
    </q-page-container>
      <q-page-container>
      <Currentdate />
    </q-page-container>   
      <q-page-container>
      <Bar />  <Dropdown/>
    </q-page-container> 
    <q-space ></q-space>  
 <q-page-container>
  <TimeDropDown/>
</q-page-container> 

<!-- <q-page-container>
  <ShareDataSet/>
</q-page-container> -->

<q-page-container>
  <LogSummary/>
</q-page-container>




 <Popup>
  
</Popup> 


  
  </q-layout>
   

</template>

<script>
import { ref } from 'vue'
import Date from '../src/views/Date.vue'
import Dashboard from '../src/views/Dashboard.vue'
import Bar from '../src/views/Bar.vue'
import Stackedline from '../src/views/Stackedline.vue'
import Dropdown from '../src/views/Dropdown.vue'
import Popup from '../src/views/Popup.vue'
import Currentdate from './views/Currentdate.vue'
import TimeDropDown from './views/TimeDropDown.vue'
import ShareDataSet from './views/ShareDataSet.vue'
import LogSummary from './views/LogSummary.vue'


export default {
 name: 'LayoutDefault',

  components: {
    Date,
    Dashboard,
    Bar,
    Stackedline,
    Dropdown,
    Popup,
    Currentdate,
    TimeDropDown,
    ShareDataSet,
    LogSummary,
  
},

}
</script>

