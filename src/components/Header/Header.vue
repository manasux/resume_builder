<template>  
  <header class='header flex'>
    <div class="name">
      <span class="name_first">Manas </span>
      <span class="name_second">Mishra</span>
    </div>
    
  </header>
</template>

<script>
export default{
  
}

</script>

<style>

.header {
  width: 100%;
  height: 25%;
  background-color: #333e50;
}
.flex {
  display: flex;
  justify-content: center;
  align-items: center;
}
.name{
  color: white;
  font-family: var(--font);
  font-size: 25px;
}
.name_first {
  color: #cb570c;
}
</style>