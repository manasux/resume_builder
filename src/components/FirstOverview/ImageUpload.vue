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
  width: 40%;
  height: auto;
  margin-left: 20px;
  margin-top: 20px;
  /* float: right; */
  display: flex;
  justify-content: center;
  align-items: center;
}
.image_desc > img {
  /* vertical-align: middle; */
  width: 110px;
  height: 110px;
  border-radius: 50%;
  border: 2px solid #333e50;
}
</style>