<template>
  <div class="header_input">
    <!-- Header Input Name -->
    <div class="header_input_name">
      <label for="username">Name:</label>
      <input type="text" name="username" v-model="name" />
    </div>
    <!-- Header Input Number -->
    <div class="header_input_phone">
      <label for="phoneno">Phone No.:</label>
      <input type="number" name="phoneno" v-model="phone" />
    </div>
    <!-- Header Input Email -->
    <div class="header_input_phone">
      <label for="email">Email:</label>
      <input type="email" name="email" v-model="email" />
    </div>
    <!-- submit btn -->
    <button class="btn submit_btn" @click="submit_header()">Submit</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: 'Manas Mishra',
      phone: '6202286832',
      email: 'mk1316a@gmail.com',
    };
  },
  methods: {
    submit_header() {
      this.$emit('inputeHeader', this.name, this.phone, this.email);
    },
  },
};
</script>

<style scoped></style>
