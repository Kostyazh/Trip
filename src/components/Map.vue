
<template>
  <div class="container">
    <div id="map">
      <button>
        <!-- <button v-on:click="visible=!visible"> -->
        Hide The Map
        <!-- {{visible?'Hide The Map':'The Map'}} -->
        <span>>></span>
      </button>
    </div>
  </div>
</template>

<script>
// const app = new Vue({
//   el: "#map",
//   data: {
//     visible: true,
//   },
// });
//  --Vue undefined--
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