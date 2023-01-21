<script>
export default {
    name: 'AppHeader',
};
</script>

<template lang="">
    <header>
        <div class="container-fluid">
            <div class="row">
                <div class="col-12 d-flex justify-content-center text-center">
                    <img  class="mt-4 position-relative py-2 px-4 text-bg-dark border border-dark rounded-pill " src="https://upload.wikimedia.org/wikipedia/commons/1/11/Yu-Gi-Oh%21_%28Logo%29.jpg" alt="">
                      
                </div>
            </div>
        </div>
    </header>
</template>

<style lang="scss" scoped>
@use "../components/styles/partials/mixins" as *;
@use "../components/styles/partials/variables" as *;


header{
    height: 50px;
    background-color: $primary;

    img{
        width: 55em;
        height: 15em;
    }
}


</style>