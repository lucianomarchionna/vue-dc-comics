<template>
  <div class="banner">
      <img src="@/assets/img/jumbotron.jpg" alt="jumbotron">
  </div>
</template>

<script>
export default {
    name: "Banner",
}
</script>

<style scoped lang="scss">
@import "@/style/generals";
.banner{
    width: 100%;
    height: 400px;

    img{
        width: 100%;
        height: 100%;
        object-position: top;
        object-fit: cover;
    }
}
</style>