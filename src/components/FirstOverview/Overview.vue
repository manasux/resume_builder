<template>
  <div class="overview">
    <span contenteditable="true" class="overview_desc">
      {{ overview }}
    </span>
  </div>
</template>

<script>
export default {
  components: {
    props: ['overview'],
  },
};
</script>

<style scoped>
.overview {
  width: 100%;
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
