<template>
  <div>
    <ul class="list" ref="list">
      <li class="item">item01</li>
      <li class="item">item02</li>
      <li class="item">item03</li>
    </ul>
  </div>
</template>

<script>
import dragula from "dragula";
export default {
  mounted() {
    dragula([this.$refs.list]) // must array;
  }
};
</script>

<style scoped lang="scss">
.list {
  padding: 0;
}
.item {
  background-color: rgba(#000, 0.3);
  cursor: grab;
  list-style: none;
  margin: 10px;
  padding: 10px;
}
</style>
