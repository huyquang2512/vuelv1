<template>
  <div id="app">
    <input type="text" v-model="ten" :disabled="lock">
    <button @click="lock = !lock"> khóa</button>
    <br>
    <div :class="{doimau: color}">
      {{ ten}}
    </div>
     <button @click="color = !color"> Đổi màu</button>

    <!-- an hien -->
    <br><br><br>
    <div v-show="show">
    <div style="width: 40px; height: 40px; background-color: red" ></div>
    <div style="width: 40px; height: 40px; background-color: blue" ></div>
    <div style="width: 40px; height: 40px; background-color: black" ></div>
    <div style="width: 40px; height: 40px; background-color: yellow" ></div>
    <div style="width: 40px; height: 40px; background-color: green" ></div>
    <div style="width: 40px; height: 40px; background-color: pink" ></div>
    </div>
    <button @click="show = !show"> Ẩn hiện</button>
  </div>
</template>

<script>

export default {
  name: 'App',
  data(){
    return {
      ten: 'Luu Quang Huy',
      lock: true,
      color: true,
      show: true
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.doimau{
  background-color: aqua;
}
</style>
