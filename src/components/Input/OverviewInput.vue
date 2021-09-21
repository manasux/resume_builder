<template>
  <div class="header_input">
    <!-- overview texfield -->
    <div class="flex_input overview_input">
      <label for="overview">Overview</label>
      <input name="overview" cols="30" rows="10" v-model="overview_text" />
      <div class="btn_flex">
        <button class="btn submit_btn" @click="submit_overview()">
          Submit
        </button>
        <button class="btn clear_btn" @click="close()">Close</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  emits: ['closeInput'],
  data() {
    return {
      overview_text:
        " Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. Lorem Ipsum is simply dummy text of the printing and typesetting industry.",
    };
  },
  methods: {
    submit_overview() {
      this.$emit('inputOverview', this.overview_text);
    },
    close() {
      this.$emit('closeInput');
    },
  },
};
</script>

<style></style>
