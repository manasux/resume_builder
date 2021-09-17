<template>
  <div class="highlights">
    <!-- Highlights Title -->
    <div class="highlights_title">
      <span>Highlights</span>
    </div>
    <!-- Highlights Description -->
    <div class="heighlights_desc">
      <ul class="heighlights_desc_ul">
        <li>Result Oriented</li>
        <li>Revenue Generation</li>
        <li>Business Development</li>
        <li>Effective Marketing</li>
        <li>Organisational Capacity</li>
        <li>Operability and commitement</li>
        <li>Resistence to stress</li>
        <li>Good Manners</li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.highlights {
  height: auto;
  width: 100%;
}
.highlights_title {
  margin-top: 30px;
  margin-left: 30px;
  font-size: 20px;
  font-family: var(--font);
  color: #cb570c;
}
.heighlights_desc {
  margin-top: 10px;
  margin-left: 30px;
  font-family: var(--font_sans);
}
.heighlights_desc_ul > li {
  font-size: 15px;
}
</style>
