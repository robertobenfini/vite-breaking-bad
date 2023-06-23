<script>
import axios from 'axios';

import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppSelect from './components/AppSelect.vue';

import { store } from './store.js';

export default {
  components:{
    AppHeader,
    AppMain,
    AppSelect
  },
  data(){
    return{
      store
    }
  },
  mounted(){
    this.getPokemonTypes()
  },
  methods:{
    getPokemonTypes(){

      let myUrl=store.apiUrl;

      if(store.typeValue !== ''){
        myUrl += `&eq[type1]=${store.typeValue}`
      }

      axios.get(myUrl).then((response) => {
      store.arrayCards = response.data.docs;
      store.loading = false;
    })
    }
  }
}
</script>

<template>
  
  <div>
    
    <AppHeader @typeChange="getPokemonTypes"/>
    <AppMain />

  </div>

</template>

<style lang="scss">
  @use './styles/generals.scss' as *;
  @use './styles/partials/variables' as *;
</style>