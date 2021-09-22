<template>
  <div class="experience">
    <ul>
      <li class="experince_li">
        <!-- Experience Title -->
        <div class="experience_title">
          <span>{{ experience_title_name }}</span>
        </div>
        <!-- Experience Description -->
        <div class="experience_desc">
          <!-- Experience Description title -->
          <div class="experience_desc_title">
            <span>
              {{ experience_company_name }}
            </span>
          </div>
          <!-- Experience Description role -->
          <div class="experience_desc_date">
            <span class="start_date"
              >{{ start_month }} {{ start_year }} -
            </span>
            <span class="end_date">{{ end_month }} {{ end_year }}</span>
          </div>
          <!-- Experience Description role -->
          <div class="experience_desc_role">
            <span>ML Engineer</span>
          </div>
          <div class="experience_todo_points">
            <ul class="experience_todo_ul">
              <li>
                Utilized PySpark to distribute data processing on large
                streaming datasets to improve ingestion and processing speed of
                that daat by 87%
              </li>
              <li>
                Build basic ETL that ingested transactional and event data from
                a web app with 10,000 daily active users that saved over $85,000
                annually in external vendor costs%
              </li>
            </ul>
          </div>
        </div>
      </li>
    </ul>
    <!-- Experience todo points -->
  </div>
</template>

<script>
export default {
  data() {
    return {
      experience_title_name: 'Experience',
      experience_company_name: 'Ozone AI',
      start_month: 'April',
      start_year: '2019',
      end_month: 'June',
      end_year: '2009',
    };
  },
};
</script>

<style>
.experience {
  height: auto;
  width: 70%;
  border-right: 1px solid #333;
}
.experince_li {
  list-style: none;
}
.experience_title {
  margin-top: 30px;
  margin-left: 30px;
  font-size: 20px;
  font-family: var(--font);
  color: #cb570c;
}
.experience_desc {
  margin-top: 10px;
  margin-left: 30px;
}
.experience_desc_title > span {
  font-family: var(--font_sans);
  font-weight: 600;
  font-size: 18px;
}
.experience_desc_role > span {
  font-family: var(--font_sans);
  font-weight: 600;
  font-size: 13px;
  color: #888;
}
.experience_desc_date > span {
  font-family: var(--font_sans);
  font-weight: 600;
  font-size: 13px;
  color: #888;
}
.experience_todo_points {
  margin-top: 10px;
  margin-left: 45px;
  margin-right: 30px;
}
.experience_todo_ul > li {
  font-family: var(--font_sans);
  font-size: 14px;
  line-height: 20px;
  margin-bottom: 5px;
}
</style>
