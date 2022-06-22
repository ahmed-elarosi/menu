<template>
  <div id="app">
    <h1 class="headline">Menu</h1>
    <Menu />
  </div>
</template>

<script>
import Menu from "./components/Menu.vue";
import './styles/app.css'
export default {
  name: "App",
  components: {
    Menu,
  },
  mounted() {},
};
</script>
