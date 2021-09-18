<template>
  <header class="header flex">
    <!-- Name -->
    <div class="name">
      <span class="name_second">
        {{ name }}
      </span>
    </div>
    <!-- phone number -->
    <div class="phone">
      <span class="phone_number"> +91 6202286832 </span>
    </div>
    <!-- Email -->
    <div class="email">
      <span class="email_desc"> amr13mk@gmail.com </span>
    </div>
  </header>

  <!-- ------------------------------------- -->

  <!-- Input -->
  <div class="input_main_header">
    <div class="input_header">
      <div class="name">
        <label for="name">Name</label>
        <input type="text" name="name" class="name_input" v-model="new_input" />
        <button class="btn_add_name" @click="add_click">Add</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: 'Manas Mishra',
      new_input: '',
    };
  },
  methods: {
    add_click() {
      this.name = this.new_input;
      this.new_input = '';
    },
  },
};
</script>

<style>
@import './Header.css';

.input_header {
  width: 60%;
  display: flex;
  height: 60%;
}
</style>
