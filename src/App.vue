<template>
  <div id="app">
    <HeaderComponent></HeaderComponent>
    <ResultHotel></ResultHotel>
  </div>
</template>

<script>
import HeaderComponent from "./components/header/header.component.vue";
import ResultHotel from "./components/result-hotel/result-hotel.component.vue";

export default {
  name: "app",
  components: {
    HeaderComponent,
    ResultHotel
  }
};
</script>

<style>
#app {
  font-family: 'Montserrat', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
</style>
