<template>
    <div class="q-pa-xl row items-start q-gutter-md">
        <q-card class="my-card">

            <q-card-section>
                <div class="text-h5">Log summary </div>
                <div>24 Hours</div>
            </q-card-section>
            <q-card>
                <q-card-section class="q-pa-sm">
                    {{ Totallogs }}<br>
                    Total Logs
                    <q-linear-progress height:10px :value="progress1" color="black">
      
    </q-linear-progress>
                </q-card-section>
                <q-card-section class="q-pa-sm">
                    {{ Errorlogs }}<br>
                    Error Logs
                    <q-linear-progress height:10px :value="progress2" color="red"/>
                </q-card-section>
                <q-card-section class="q-pa-sm">
                    {{ Warnlogs }}<br>
                    Warn Logs
                    <q-linear-progress height:10px :value="progress3" color="yellow"/>
                </q-card-section>
                <q-card-section class="q-pa-sm">
                    {{ Fatallogs }}<br>
                    Fatal Logs
                    <q-linear-progress height:10px :value="progress4" color="orange"/>
                </q-card-section>
            </q-card>
        </q-card>


    </div>
</template>
  
<script>
import { ref, computed } from 'vue'
export default {
    
    setup() {
        const progress1 = ref(100)
        const progress2 = ref(.7)
        const progress3 = ref(.4)
        const progress4 = ref(.7)
        return {
            Totallogs: '92.5K',
            Errorlogs: '18k',
            Warnlogs: '35k',
            Fatallogs: '12k',
            progress1,
            progressLabel1: computed(() => (progress1.value * 100).toFixed(2) + '%'),
            progress2,
            progressLabel1: computed(() => (progress2.value * 100).toFixed(2) + '%'),
            progress3,
            progressLabel1: computed(() => (progress3.value * 100).toFixed(2) + '%'),
            progress4,
            progressLabel1: computed(() => (progress4.value * 100).toFixed(2) + '%'),


        }
     
    }
}
</script>
  
<style lang="sass" scoped>
  .my-card
    height: 380px
    width: 100%
    max-width: 180px
    border-radius: 25px
    .h_line_total 
      border-bottom: 6px solid rgb(80, 80, 78)
      

    .h_line_error 
      border-bottom: 6px solid rgb(255, 0, 0)
      width: 25px  

    .h_line_warn
      border-bottom: 6px solid rgb(255, 223, 0)
      width: 40px   

    .h_line_fatal
      border-bottom: 6px solid rgb(220, 20, 60)
      width: 30px    
 

  
  </style>
  