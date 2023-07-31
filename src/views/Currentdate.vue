<script>

export default {
    data() {
        return {
            date: ''
        }
    },
    methods: {
        getCurrentDate() {

            var today = new Date();

            var dd = String(today.getDate()).padStart(2, '0');

            var mm = String(today.getMonth() + 1).padStart(2, '0');

            var yyyy = today.getFullYear();

            today = mm + '/' + dd + '/' + yyyy;

            this.date = today

          

        },



        // checkDate (val) {

        //   return Quasar.utils.date.isValid(val) || 'Invalid date.'

        // },



    },

    beforeMount() {

        this.getCurrentDate()

    },
}

</script>

  
<template>
    <div id="q-app">

        <div class="q-pa-md" style="max-width: 300px">

            <q-input filled v-model="date" mask="##/##/####">

                <template v-slot:append>

                    <q-icon name="event" class="cursor-pointer">

                        <q-popup-proxy ref="qDateProxy" transition-show="scale" transition-hide="scale">

                            <q-date v-model="date" @input="() => $refs.qDateProxy.hide()" mask="MM/DD/YYYY"></q-date>

                        </q-popup-proxy>

                    </q-icon>

                </template>

            </q-input>

        </div>

    </div>
</template>