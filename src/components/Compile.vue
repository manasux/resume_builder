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
              <Overview
                @openOverviewEdit="openOverview"
                :overview="newOverview"
              ></Overview>
            </div>
            <hr />
            <!-- resume details -->
            <div class="bottom">
              <Experience
                :experienceTitleName="experience_title_name"
                :experienceCompanyName="experience_company_name"
                :startMonth="start_month"
                :startYear="start_year"
                :endYear="end_year"
                :experienceRole="experience_role"
                :experienceDescOne="experience_desc_one"
                :experinceDescTwo="experience_desc_two"
              ></Experience>
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

  <!-- header_input -->
  <div class="main_resume_input" v-if="openChange == 1 && open">
    <div class="header_resume_input">
      <HeaderInput
        @inputeHeader="updateHeader"
        @closeInput="closingInput"
      ></HeaderInput>
    </div>
  </div>

  <!-- Overview input -->
  <div class="main_resume_input" v-if="openChange == 2 && open">
    <div class="overview_resume_input">
      <OverviewInput
        @inputOverview="updateOverview"
        @closeInput="closingInput"
      ></OverviewInput>
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
import OverviewInput from './Input/OverviewInput.vue';

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
    OverviewInput,
  },
  data() {
    return {
      newName: 'Manas Mishra',
      newContact: '6202286832',
      newEmail: 'mk1316a@gmail.com',
      newOverview:
        ' Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industrys standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. Lorem Ipsum is simply dummy text of the printing and typesetting industry.',
      // experince
      experience_title_name: 'Experience',
      experience_company_name: 'Ozone AI',
      start_month: 'April',
      start_year: '2019',
      end_month: 'June',
      end_year: '2009',
      experience_role: 'ML Engineer',
      experience_desc_one:
        'Utilized PySpark to distribute data processing on large streaming datasets to improve ingestion and processing speed of that daat by 87%',
      experience_desc_two:
        'Build basic ETL that ingested transactional and event data from a web app with 10,000 daily active users that saved over $85,000 annually in external vendor costs',

      // common
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
      this.open = false;
    },
    closingInput() {
      this.open = false;
    },
    openHeader() {
      this.openChange = 1;
      this.open = !this.open;
    },
    openOverview() {
      this.openChange = 2;
      this.open = !this.open;
    },
    updateOverview(var1) {
      this.newOverview = var1;
      this.open = false;
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
.overview_resume_input {
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
