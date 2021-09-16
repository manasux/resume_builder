<template>  
  <div class="resume_template">
    <Header></Header>
  </div>
</template>

<script>
import Header from "./Header/Header.vue";
export default{
  components: {
    Header,
  },
}

</script>

<style>
  .resume_template {
    width: 50vw;
    height: 100vh;
  }
</style>