<template>  
  <div class="resume_template">
  <!-- Header -->
    <Header></Header>
    <!-- First Overview -->
    <div class="first_overview">
      <!-- Overview -->
      <Overview></Overview>
      <!-- image upload -->
      <ImageUpload></ImageUpload>
    </div>
    <hr>
    <div class="bottom">
      <Experience></Experience>
      <Highlights></Highlights>
    </div>
  </div>
</template>

<script>
import Header from "./Header/Header.vue";
import Overview from "./FirstOverview/Overview.vue";
import ImageUpload from "./FirstOverview/ImageUpload.vue";
import Experience from "./Second/Experience.vue";
import Highlights from "./Second/Highlights.vue";

export default{
  components: {
    Header,
    Overview,
    ImageUpload,
    Experience,
    Highlights,
  },
}

</script>

<style>
hr{
  margin-top: 10px;
}
  .resume_template {
    width: 50vw;
    height: 100vh;
  }
  .first_overview{
    display: flex;
  }
  .bottom{
    display: flex;
  }
</style>