<template>
  <div id="app">
    <div class="wrap">
      <div class="left">
        <Navbar />
        <Filters />
        <Day v-bind:element="element" />
        <Description v-bind:element="element" />
      </div>
      <Map v-bind:element="element" />
    </div>
    <div class="container">
      <router-view />
    </div>
  </div>
</template>

<script>
import Navbar from "@/components/HomeComponents/Navbar";
import Map from "@/components/HomeComponents/Map";
import Description from "@/components/HomeComponents/Description";
import Filters from "@/components/HomeComponents/Filters";
import Day from "@/components/Day";
const userData = require("../response.json");
console.log(userData);
export default {
  data() {
    return {
      element: userData,
    };
  },
  components: { Navbar, Map, Description, Filters, Day },
};
</script>

<style lang="scss" scoped>
.wrap {
  display: flex;
  justify-content: center;
  width: 100%;
}
</style>