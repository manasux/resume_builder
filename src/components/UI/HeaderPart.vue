<template>
  <div class="header_part">
    <div class="logo">
      <img
        src="https://cdn.dribbble.com/users/24078/screenshots/15522433/media/e92e58ec9d338a234945ae3d3ffd5be3.jpg?compress=1&resize=400x300"
        alt="logo"
        class="logo"
      />
    </div>
    <div class="buttons">
      <button class="btn btn_reset">Reset</button>
      <button class="btn btn_download">Download</button>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.header_part {
  height: 15vh;
  width: 100%;
  background-color: #000000;
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.logo {
  height: 90px;
}
.buttons {
  margin-right: 100px;
}
</style>
