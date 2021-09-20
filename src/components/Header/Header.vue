<template>
  <header class="header flex">
    <!-- Name -->
    <div class="name">
      <span class="name_second">
        {{ name }}
      </span>
      <button @click="changenameCounter()" class="btn btn_icon">
        <i class="fas fa-pen"></i>
      </button>
    </div>
    <!-- phone number -->
    <div class="phone">
      <span class="phone_number"> +91 6202286832 </span>
    </div>
    <!-- Email -->
    <div class="email">
      <span class="email_desc"> amr13mk@gmail.com </span>
    </div>
  </header>

  <!-- ------------------------------------- -->

  <!-- Input -->
  <div v-if="counter == 1 && active" class="input_main_header">
    <div class="input_header">
      <div class="name">
        <label for="name">Name</label>
        <input type="text" name="name" class="name_input" v-model="new_input" />
        <button class="btn_add_name" @click="add_click">Add</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: 'Manas Mishra',
      new_input: '',
      counter: 0,
      active: false,
    };
  },
  methods: {
    add_click() {
      this.name = this.new_input;
      this.new_input = '';
    },
    changenameCounter() {
      this.counter = 1;
      this.active = !this.active;
    },
  },
};
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
.name {
  color: white;
  font-family: var(--font);
  font-size: 35px;
  display: flex;
  /* flex-direction: column; */
  justify-content: center;
  align-items: center;
}
.name_second {
  color: #fff;
}
.phone_number {
  color: #fff;
  font-size: 15px;
  font-family: var(--font_roboto);
}
.email_desc {
  color: #fff;
  font-family: var(--font_roboto);
}
.input_header {
  width: 60%;
  display: flex;
  height: 60%;
}
.btn_icon {
  width: 20px;
  height: 20px;
  margin-left: 20px;
  border: 0.2px solid black;
  border-radius: 5px;
  background: #fc30ef;
  color: #fff;
  font-size: 10px;
  cursor: pointer;
}
</style>
