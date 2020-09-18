<template>
  <div id="app">
    <div class="container">
      <router-view />
    </div>
  </div>
</template>

<script >
import Map from "@/components/Map";
import Navbar from "@/components/Navbar";

export default {
  components: { Navbar, Map },
};
</script>

<style lang="scss" scoped>
</style>
