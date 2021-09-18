<template>
  <div class="header_input">
    <!-- Input Header -->
    <div class="input_header">
      <!-- Input Name -->
      <div class="input_name_div flex_input">
        <label for="name">Name</label>
        <input
          type="text"
          class="name_input"
          name="name"
          v-model="resume_name"
        />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      resume_name: 'Manas',
    };
  },
};
</script>

<style>
.header_input {
  width: 100%;
  height: 100%;
  margin-left: 30px;
  margin-top: 20px;
  /* background: #333; */
}
.flex_input {
  display: flex;
  flex-direction: column;
}
input {
  width: 30%;
}
</style>
