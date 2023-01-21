<script>
export default {
  props: {
    card: Object,
  },
  data() {
    return {
      index: 0,
    };
  },
};
</script>

<template lang="">
    <div class="col-12 col-md-4 mt-3">
        <div class="cards-card">
            <img class="img-fluid" :src="card.card_images[0].image_url">
            <div class="card-info">
                <h4>{{ card.name }}</h4>
                <p>{{ card.type }}</p>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use "../components/styles/partials/variables" as *;
.cards-card {
  background-color: $primary;
  width: 100%;
  height: 100%;
  text-align: center;
 


  h4 {
    text-transform: uppercase;
    color: white;
  }

  .card-info{
    padding: 10px;
  }
}
</style>