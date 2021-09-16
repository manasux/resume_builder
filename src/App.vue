<template>
  <div class="main_body">
    <Compile></Compile>
  </div>
</template>

<script>
import Compile from "./components/Compile.vue"
export default {
  components: {
    Compile,
  }
}
</script>

<style>
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
.main_body{
  height: 100vh;
  width: 100vw;
}
</style>
