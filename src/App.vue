<template>
  <div id="app">
    <Drag />
  </div>
</template>

<script>
import Drag from "./components/Drag";

export default {
  name: "app",
  components: {
    Drag
  }
};
</script>

<style>
@import "../node_modules/dragula/dist/dragula.min.css";
</style>
