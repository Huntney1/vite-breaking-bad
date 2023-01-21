<script>
export default {
    
}
</script>

<template lang="">
    <div class="loader-bkg">
      <div class="lds-dual-ring">Yu-Gi-Oh</div>
    </div>
</template>

<style lang="scss" scoped>
@use "../components/styles/partials/variables" as *;

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
  width: 80px;
  height: 80px;
}
.lds-dual-ring:after {
  content: " ";
  display: block;
  width: 64px;
  height: 64px;
  margin: 8px;
  border-radius: 50%;
  border: 6px solid #fff;
  border-color: #fff transparent #fff transparent;
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