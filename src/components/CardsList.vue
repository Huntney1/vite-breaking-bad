<script>
import CharacterCard from './CharacterCard.vue';
import { store } from '../store.js';

export default {
components:{
    CharacterCard
},
    data() {
        store
    },
}
</script>

<template lang="">
  <main class="container">
    <div class="row">
        Carte trovate: {{ store.cardsList.length }}
    </div>
     <div class="row">
        <div class="col-12">
            <CaracterCard v-for="(item, index) in store.cardsList" :key="index" :card="item" />
        </div>
     </div>
  </main>
</template>

<style lang="scss" scoped>
@use "../components/styles/partials/mixins" as *;
@use "../components/styles/partials/variables" as *;

main{
    background-color: white;
    margin-top:2.5em;
}    

</style>