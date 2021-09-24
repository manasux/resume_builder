<template>
  <div class="hobbies">
    <!-- Education Title -->
    <div class="hobbies_title">
      <span>{{ title }}</span>
      <!-- submit btn -->
      <div @click="edit_hobbie()" class="header_edit">
        <button class="btn btn_change"><i class="fas fa-pen"></i></button>
      </div>
    </div>
    <!-- Hobbies Description -->
    <div class="hobbies_desc">
      <ul class="hobbies_desc_ul" contenteditable="true">
        <li>Playing Chess</li>
        <li>Reading books</li>
        <li>Listening Music</li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  props: ['title'],
  methods: {
    edit_hobbie() {
      this.$emit('openHobbiesEdit');
    },
  },
};
</script>

<style scoped>
.hobbies_title {
  margin-top: 30px;
  margin-left: 30px;
  font-size: 20px;
  font-family: var(--font);
  color: #cb570c;
  display: flex;
}
.hobbies_desc {
  margin-left: 30px;
  margin-top: 10px;
}
.hobbies_desc_ul {
  font-family: var(--font_sans);
}
.hobbies_desc_ul > li {
  color: #333;
  font-size: 14px;
}
</style>
