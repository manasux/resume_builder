<template>
  <!-- Main header -->
  <div class="main_resume_template">
    <div class="main_header">
      <HeaderPart @downloadtopdf="changeT()"></HeaderPart>
    </div>

    <div>
      <div class="main_body_template">
        <div class="main_template">
          <div class="resume_template" id="convert">
            <!-- Header Resume-->
            <div class="header_resume">
              <Header
                @openHeaderEdit="openHeader"
                :name="newName"
                :contact="newContact"
                :email="newEmail"
              ></Header>
            </div>
            <!-- First Overview -->
            <div class="first_overview">
              <!-- Overview -->
              <Overview></Overview>
            </div>
            <hr />
            <!-- resume details -->
            <div class="bottom">
              <Experience></Experience>
              <!-- Right side of resume details -->
              <div class="second_part">
                <Highlights></Highlights>
                <Education></Education>
                <Hobbies></Hobbies>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <div class="main_footer">
      <FooterPart></FooterPart>
    </div>
  </div>
  <div class="main_resume_input" v-if="open">
    <div class="header_resume_input" v-if="openChange == 1">
      <HeaderInput @inputeHeader="updateHeader"></HeaderInput>
    </div>
  </div>
</template>

<script>
import Header from './Header/Header.vue';
import Overview from './FirstOverview/Overview.vue';
import Experience from './Second/Experience.vue';
import Highlights from './Second/Highlights.vue';
import Education from './Second/Education.vue';
import Hobbies from './Second/Hobbies.vue';
import HeaderPart from './UI/HeaderPart.vue';
import FooterPart from './UI/FooterPart.vue';
import HeaderInput from './Input/HeaderInput.vue';

export default {
  components: {
    Header,
    Overview,
    Experience,
    Highlights,
    Education,
    Hobbies,
    HeaderPart,
    FooterPart,
    HeaderInput,
  },
  data() {
    return {
      newName: 'Manas Mishra',
      newContact: '6202286832',
      newEmail: 'mk1316a@gmail.com',
      openChange: 0,
      open: false,
    };
  },
  methods: {
    changeT() {
      var element = document.getElementById('convert');
      html2pdf(element);
    },
    updateHeader(var1, var2, var3) {
      this.newName = var1;
      this.newContact = var2;
      this.newEmail = var3;
      this.open = !this.open;
    },
    openHeader() {
      this.open = !this.open;
      this.openChange = 1;
    },
  },
};
</script>

<style scoped>
hr {
  margin-top: 10px;
}
.main_resume_template {
  width: 100vw;
  height: auto;
}
.main_template {
  width: 50vw;
  height: 80%;
}

.resume_template {
  width: 100%;
  height: 100%;

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
.main_body_template {
  display: flex;
  justify-content: center;
  align-items: center;
}
#convert {
  outline: none;
}
.main_resume_input {
  display: flex;
  justify-content: center;
  align-items: center;
  transform: translateY(-90vh);
  /* background: lightcoral; */
  height: 60vh;
}
.header_resume_input {
  display: flex;
  justify-content: center;
  width: 60vw;
  border: 1px solid black;
  height: 100%;
  align-items: center;
  background: #001559;
  border-radius: 10px;
  opacity: 1;
}
</style>
