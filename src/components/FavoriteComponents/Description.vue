<template>
  <div class="container_body">
    <Body v-for="element in element.slice(0, 6)" v-bind:element="element" />
  </div>
</template>

<script>
// const userData = require("../response.json");
// console.log(userData);
import Body from "@/components/FavoriteComponents/Body";

export default {
  props: ["element"],
  components: {
    Body,
  },
};
</script>

<style lang="scss" scoped>
.container_body {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  width: 1000px;
  height: 200px;
}
</style>