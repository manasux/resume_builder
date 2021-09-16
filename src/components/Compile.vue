<template>  
  <div class="resume_template">
    <Header></Header>
    <div class="first_overview">
      <Overview></Overview>
      <ImageUpload></ImageUpload>
    </div>
  </div>
</template>

<script>
import Header from "./Header/Header.vue";
import Overview from "./FirstOverview/Overview.vue";
import ImageUpload from "./FirstOverview/ImageUpload.vue";

export default{
  components: {
    Header,
    Overview,
    ImageUpload,
  },
}

</script>

<style>
  .resume_template {
    width: 50vw;
    height: 100vh;
  }
</style>