<template>  
  <div class="overview">
    <span class="overview_desc">
      Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. Lorem Ipsum is simply dummy text of the printing and typesetting industry.
    </span>
  </div>
</template>

<script>
export default{
  components: {
    
  },
}

</script>

<style scoped>
.overview{
  width: 60%;
  height: auto;
  margin-left: 10px;
  margin-top: 20px;
  display: flex;
  justify-content: center;
  align-items: center;
}
.overview_desc {
  font-family: var(--font_roboto);
  font-size: 13px;
  line-height: 22px;
}
</style>