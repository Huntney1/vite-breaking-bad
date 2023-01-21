<script>
import AppHeader from "./components/AppHeader.vue";
import AppMain from "./components/AppMain.vue";
import Loader from "./components/Loader.vue";


import axios from "axios";
import { store } from "./store.js";

export default{
  components:{
    AppHeader,
    AppMain,
    Loader,
  },
  /* richiamo la lista in cardsList */
  data() {
    return {
      store
    }
  },
  created(){
    this.getCardsList();
  },
   methods: {
    getCardsList(){
      axios.get(store.url).then((response) => {
        store.cardsList = response.data.data;
        setTimeout(() => {
          store.isLoaded = true;
        },4000)
        
      });
    }
  }, 
}

</script>

<template lang="">
  <div v-if="store.isLoaded">
    <AppHeader />
    <AppMain />
  </div>
  <div v-else>
    <Loader />
  </div>
</template>

<style lang="scss">
@use "./components/styles/generals.scss" as *;
</style>
