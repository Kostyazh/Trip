<template>
  <div class="container">
    <Body v-for="element of element" v-bind:element="element" />
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
.container {
  width: 710px;
  height: 200px;
}
</style>