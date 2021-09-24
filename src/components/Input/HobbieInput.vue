<template>
  <div class="hobbie_input">
    <!-- Hobbie Input title -->
    <div class="highlight_input_title flex_input">
      <label for="title">Title:</label>
      <input
        type="text"
        name="title"
        class="change_input"
        autocomplete="off"
        v-model="title"
      />
    </div>
    <!-- submit btn -->
    <div class="btn_flex">
      <button class="btn submit_btn" @click="submit_hobbies()">Submit</button>
      <button class="btn clear_btn" @click="close()">Close</button>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      title: '',
    };
  },
  methods: {
    submit_hobbies() {
      this.$emit('inputHobbie', this.title);
      // this.highlight_list = '';
    },
    close() {
      this.$emit('closeInput');
    },
  },
};
</script>

<style></style>
