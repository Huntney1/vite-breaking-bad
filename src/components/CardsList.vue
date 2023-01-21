<script>
import CharacterCard from "./CharacterCard.vue";
import { store } from "../store.js";

export default {
    name: 'CardsList',
    /* props:{
        option: Object

    }, */
components:{
    CharacterCard,
    option: Object
},
    data() {
        return{
             store,
             change: '',
        }
       
    },
}
</script>

<template lang="">
  <main class="container">

    <div class="container-select">
        <select class="select-style mt-4" id="" name="alien" v-model="change" @change="$emit('selectchangeName', change)">
            <option value="">Seleziona un Archetipo</option>
            <option v-for="(element, index) in option" :key="index" value="element.archetype_name">{{ element.archetype_name }}</option>
        </select>
    
        <div class="cont-num">
            Carte trovate: {{ store.cardsList.length }}
        </div>
    </div>

     <div class="row">
            <CharacterCard v-for="(item, index) in store.cardsList" :key="index" :card="item" />
     </div>
  </main>
</template>

<style lang="scss" scoped>
@use "../components/styles/partials/mixins" as *;
@use "../components/styles/partials/variables" as *;

main{
    background-color: white;
    margin-top: 11em;

}    
    .select-style{
        background-color: black;
        width: 14em;
       /*  height: 100%; */
        color: white;
        border: none;
       
    }

    .container-num{
        display: flex;
        align-items: center;
        padding: 0 1rem;
        background-color: black;
        color: white;
        height: 100%;

        h4{
            color: white;
        }
    }



</style>