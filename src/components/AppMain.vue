<script>

import AppCards from './AppCards.vue';

import { store } from '../store.js'

export default {
    components:{
        AppCards
    },
    data(){
        return{
            store
        }
    }
}
</script>

<template>
    
    <main>
       <div class="container bg-white p-5 mt-3 rounded">
            <div class="row d-flex bg-secondary overflow-auto h-row">
                <div v-for="(card, index) in store.arrayCards" :key="index" class="col-lg-2 col-md-4 col-sm-6">
                    <AppCards :myCard="card" />
                </div>
            </div>
       </div> 
    </main>

</template>

<style lang="scss" scoped>
    .h-row{
        height: 500px;
    }
</style>