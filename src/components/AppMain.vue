<script>
import CardsList from "./CardsList.vue"

export default {
    components:{
        CardsList
    }
}
</script>

<template lang="">
    <div>
        <CardsList />
    </div>
</template>

<style lang="scss" scoped>
@use "../components/styles/partials/mixins" as *;
@use "../components/styles/partials/variables" as *;

</style>