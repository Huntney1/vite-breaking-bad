<script>
import AppHeader from "./components/AppHeader.vue";
import AppMain from "./components/AppMain.vue";
import AppMain from "./components/AppMain.vue";

import axios from "axios";
import { store } from "./store.js";

export default{
  components:{
    AppHeader,
    AppMain,
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
      });
    }
   }, 
}

</script>

<template lang="">
<AppHeader />
<AppMain />
   
</template>

<style lang="scss">
@use "./components/styles/generals.scss" as *;
</style>
