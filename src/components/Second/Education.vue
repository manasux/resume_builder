<template>
  <div class="education">
    <!-- Education Title -->
    <div class="education_title">
      <span>Education</span>
    </div>
    <!-- Education Description -->
    <div class="education_desc">
      <ul class="education_desc_ul">
        <li>
          <span class="education_desc_degree_name">Bachelor of Science,</span>
          <br />
          <span class="education_desc_course_name">Automotive Technology,</span>
          <br />
          <span class="education_desc_uni_name">
            Kalasalingam Academy of Research and Education,
          </span>
          <br />
          <span class="education_desc_uni_place">
            Virudhanagar, Tamilnadu, India,
          </span>
          <br />
          <span class="education_desc_uni_cgpa"> 3.7 GPA </span>
          <br />
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.education_title {
  margin-top: 30px;
  margin-left: 30px;
  font-size: 20px;
  font-family: var(--font);
  color: #cb570c;
}
.education_desc {
  margin-left: 30px;
  margin-top: 10px;
}
.education_desc_ul {
  font-family: var(--font_sans);
  display: flex;
  flex-direction: column;
}
.education_desc_ul > li {
  color: #333;
  font-size: 14px;
}
.education_desc_degree_name {
  color: #000;
  font-weight: bold;
}
</style>
