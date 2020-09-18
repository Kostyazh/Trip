
<template>
  <div id="apps">
    <div class="documents" v-if="!isShow1" id="map">
      <button v-on:click="isShowText">Hide The Map</button>
    </div>
    <div class="market" v-if="isShow2" id="map2">
      <button v-on:click="isShowText">The Map</button>
    </div>
  </div>
</template>

<script>
export default {
  el: "#apps",
  data: function () {
    return {
      isShow1: false,
      isShow2: false,
    };
  },
  methods: {
    isShowText() {
      this.isShow1 = !this.isShow1;
      this.isShow2 = !this.isShow2;
    },
  },
};
</script>


<style lang="scss" scoped>
#map {
  position: relative;
  justify-content: center;
  margin: 0 10px 10px 30px;
  width: 509px;
  height: 109vh;
  background-color: rgb(238, 238, 238);
}
#map2 {
  position: relative;
  justify-content: center;
  margin: 0 10px 10px 30px;
  width: 509px;
  height: 109vh;
  background-color: none;
}
button {
  position: absolute;
  text-transform: uppercase;
  height: 40px;
  width: 200px;
  top: 22px;
  left: 68px;
  background-color: rgb(199, 199, 199);
  border: none;
  color: white;
  opacity: 0.8;
  cursor: pointer;
  span {
    color: silver;
  }
}
button:hover {
  opacity: 1;
}
button:active,
button:focus {
  outline: none;
}
button::-moz-focus-inner {
  border: 0;
}
</style>