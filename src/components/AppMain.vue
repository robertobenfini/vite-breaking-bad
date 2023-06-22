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
    
    <div>
       <div class="container">
        <div class="row d-flex justify-between">
            <div v-for="(card, index) in store.arrayCards" :key="index" class="col-2 mx-2">
                <AppCards :myCard="card" />
            </div>
        </div>
       </div> 
    </div>

</template>

<style lang="scss" scoped>
    
</style>