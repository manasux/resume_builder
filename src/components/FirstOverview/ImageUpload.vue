<template>  
  <div class="imageuploader">
    <div class="image_desc">
      <img src="https://st.depositphotos.com/1428083/2946/i/600/depositphotos_29460297-stock-photo-bird-cage.jpg" alt="image">
    </div>
  </div>
</template>

<script>
export default{
  components: {

  },
}

</script>

<style>
.imageuploader {
  width: 20%;
  height: auto;
  margin-left: 10px;
  margin-top: 20px
}
.image_desc > img {
  width: 100%;
  height: 100%;
  border-radius: 100%;
}
</style>