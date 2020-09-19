<template>
  <div class="container_body">
    <Body v-for="element in element.slice(0, 3)" v-if v-bind:element="element" />
  </div>
</template>

<script>
// const userData = require("../response.json");
// console.log(userData);
import Body from "@/components/Body";

export default {
  props: ["element"],
  components: {
    Body,
  },
};
</script>

<style lang="scss" scoped>
.container_body {
  width: 710px;
  height: 200px;
}
</style>