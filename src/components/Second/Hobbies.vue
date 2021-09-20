<template>
  <div class="hobbies">
    <!-- Education Title -->
    <div class="hobbies_title">
      <span contenteditable="true">Hobbies</span>
    </div>
    <!-- Hobbies Description -->
    <div class="hobbies_desc">
      <ul class="hobbies_desc_ul">
        <li contenteditable="true">Playing Chess</li>
        <li>Reading books</li>
        <li>Listening Music</li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.hobbies_title {
  margin-top: 30px;
  margin-left: 30px;
  font-size: 20px;
  font-family: var(--font);
  color: #cb570c;
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
