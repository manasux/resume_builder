<template>
  <div class="experience">
    <!-- Experience Title -->
    <div class="experience_title">
      <span>Experiences</span>
    </div>
    <!-- Experience Description -->
    <div class="experience_desc">
      <div class="experience_desc_title">
        <span>LearnCodeOnline</span>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style>
.experience {
  height: auto;
  width: 70%;
  border-right: 1px solid #333;
}
.experience_title {
  margin-top: 30px;
  margin-left: 30px;
  font-size: 28px;
  font-family: var(--font);
  color: #cb570c;
}
.experience_desc {
  width: 100%;
  margin-top: 10px;
  margin-left: 30px;
}
.experience_desc_title > span {
  font-family: var(--font_sans);
  font-weight: 600;
}
</style>
