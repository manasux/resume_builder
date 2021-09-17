<template>
  <div class="main_header">
    <HeaderPart></HeaderPart>
  </div>
  <div class="main_template">
    <div class="resume_template">
      <!-- Header -->
      <div class="header_resume">
        <Header></Header>
      </div>
      <!-- First Overview -->
      <div class="first_overview">
        <!-- Overview -->
        <Overview></Overview>
        <!-- image upload -->
        <ImageUpload></ImageUpload>
      </div>
      <hr />
      <div class="bottom">
        <Experience></Experience>
        <div class="second_part">
          <Highlights></Highlights>
          <Education></Education>
          <Hobbies></Hobbies>
        </div>
      </div>
    </div>
  </div>
  <div class="main_footer">
    <FooterPart></FooterPart>
  </div>
</template>

<script>
import Header from './Header/Header.vue';
import Overview from './FirstOverview/Overview.vue';
import ImageUpload from './FirstOverview/ImageUpload.vue';
import Experience from './Second/Experience.vue';
import Highlights from './Second/Highlights.vue';
import Education from './Second/Education.vue';
import Hobbies from './Second/Hobbies.vue';
import HeaderPart from './UI/HeaderPart.vue';
import FooterPart from './UI/FooterPart.vue';

export default {
  components: {
    Header,
    Overview,
    ImageUpload,
    Experience,
    Highlights,
    Education,
    Hobbies,
    HeaderPart,
    FooterPart,
  },
};
</script>

<style scoped>
hr {
  margin-top: 10px;
}
.main_template {
  width: 50vw;
  height: 80%;
}
.resume_template {
  width: 100%;
  height: 100%;
  margin: 20px;
  border: 0.5px solid #333;
}
.first_overview {
  display: flex;
}
.bottom {
  display: flex;
}
.second_part {
  width: 40%;
}
.header_resume {
  height: 50%;
}
</style>
