
<template>
  <div id="apps">
    <div class="documents" v-if="!isShow1" id="map">
      <!-- {{element[0].show_on_map}} -->
      <button v-on:click="isShowText">
        Hide The Map
        <span>>></span>
      </button>
    </div>
    <div class="market" v-if="isShow2" id="map2">
      <button v-on:click="isShowText">
        The Map
        <span>>></span>
      </button>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    element: {
      type: Object,
      required: true,
    },
  },
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
  height: 116vh;
  background-color: rgb(238, 238, 238);
}
#map2 {
  position: relative;
  justify-content: center;
  margin: 0 10px 10px 30px;
  width: 509px;
  height: 116vh;
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
    margin-left: 15px;
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