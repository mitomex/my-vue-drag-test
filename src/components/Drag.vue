<template>
  <div>
    <div v-for="item in items" :key="item.id">
      <ul class="list" ref="list">
        <li class="item">item01</li>
        <li class="item">item02</li>
        <li class="item">item03</li>
      </ul>
    </div>
  </div>
</template>

<script>
import dragula from "dragula";
export default {
  data() {
    return {
      items: [
        {
          id: 1
        }
      ]
    };
  },
  mounted() {
    /* eslint-disable no-console */
    console.log(Array.isArray(this.$refs.list)); // this.$refs.list's return value is Array, when it is used by `v-for`
    dragula(this.$refs.list); // must array
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
