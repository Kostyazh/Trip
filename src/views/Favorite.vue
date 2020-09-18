<template>
  <div id="app">
    <div class="wrap">
      <div class="left">
        <Navbar />
        <FilterHome />
        <Day v-bind:element="element" />
        <Description v-bind:element="element" />
      </div>
      <Map />
    </div>
    <div class="container">
      <router-view />
    </div>
  </div>
</template>

<script>
import Navbar from "@/components/Navbar";
import Map from "@/components/Map";
import Description from "@/components/Description";
import FilterHome from "@/components/FilterHome";
import Day from "@/components/Day";
const userData = require("../response.json");
console.log(userData);
export default {
  data() {
    return {
      element: userData,
    };
  },
  components: { Navbar, Map, Description, FilterHome, Day },
};
</script>

<style lang="scss" scoped>
.wrap {
  display: flex;
  justify-content: center;
  width: 100%;
}
</style>