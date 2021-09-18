<template>
  <div class="header_input">
    <!-- Input Header -->
    <div class="input_header">
      <!-- Input Name -->
      <div class="input_name_div flex_input">
        <label for="name">Name</label>
        <input type="text" class="name_input" name="name" v-model="new_input" />
      </div>
      <button @click="add_name_btn" class="btn_add">Add Name</button>
    </div>
    <p>{{ resume_name }}</p>
  </div>
</template>

<script>
import { EventBus } from './event-bus.js';
export default {
  data() {
    return {
      resume_name: 'Manas',
      new_input: '',
    };
  },
  methods: {
    add_name_btn() {
      this.resume_name = this.new_input;
      EventBus.$emit('clicked-event', this.Count);
    },
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
