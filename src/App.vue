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
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@600&family=Roboto&display=swap');

:root{
  --font: 'Montserrat', sans-serif;
  --font_roboto: 'Roboto', sans-serif;
}

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
