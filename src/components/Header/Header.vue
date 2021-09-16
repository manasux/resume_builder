<template>  
  <header class='header flex'>
    <!-- Name -->
    <div class="name">
      <span class="name_first">Manas </span>
      <span class="name_second">Mishra</span>
    </div>
    <!-- phone number -->
    <div class="phone">
      <span class="phone_number">
        +91 6202286832
      </span>
    </div>
    <!-- Email -->
    <div class="email">
      <span class="email_desc">
        amr13mk@gmail.com
      </span>
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
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.name{
  color: white;
  font-family: var(--font);
  font-size: 35px;
}
.name_first {
  color: #cb570c;
}
.phone_number{
  color: #fff;
  font-size: 15px;
  font-family: var(--font_roboto);
}
.email_desc{
  color: #fff;
  font-family: var(--font_roboto);
}
</style>