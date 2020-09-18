<template>
  <div id="app">
    <!-- <div class="wrap">
      <div class="left">
        <Navbar />
      </div>
      <Map />
    </div>-->
    <div class="container">
      <router-view />
    </div>
  </div>
</template>

<script>
import Navbar from "@/components/Navbar";
import Map from "@/components/Map";
export default {
  components: { Navbar, Map },
};
</script>

<style lang="scss" scoped>
</style>
