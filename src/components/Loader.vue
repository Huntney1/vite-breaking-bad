<script>
export default {
    
}
</script>

<template lang="">
  <div class="bck-img">
    <div class="loader-bkg">
      <div class="lds-dual-ring">
        <!-- <img src="https://upload.wikimedia.org/wikipedia/commons/1/11/Yu-Gi-Oh%21_%28Logo%29.jpg" alt=""> -->
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use "../components/styles/partials/variables" as *;

.bck-img {
  width: 100%;
  background-image: url("https://upload.wikimedia.org/wikipedia/commons/1/11/Yu-Gi-Oh%21_%28Logo%29.jpg");
  background-size: auto;
}

.loader-bkg{
    width: 100vw;
    height: 100vh;
    background-color: rgba(0,0,0,0.25);
    position: relative;
    top: 0;
    left: 0;
}
.lds-dual-ring {
  display: inline-block;
  width: 200px;
  height: 200px;

}
.lds-dual-ring:after {
  content: " ";
  display: block;
  width: 100px;   /* w_h: 64px */
  height: 100px;
  margin: 8px;
  border-radius: 50%;
  border: 6px solid #fff;
  border-color: rgb(249, 5, 5) transparent $primary transparent;
  position: absolute;
  top: 50%;
  left: 50%;
  animation: lds-dual-ring 1.2s linear infinite;
}
@keyframes lds-dual-ring {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}

</style>