<template>
  <div class="container">
    <button>Price</button>
    <button>Dinner</button>
    <button>Filter 1</button>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.container {
  display: flex;

  button {
    font-size: 16px;
    background-color: rgb(238, 238, 238);
    border: none;
    border-radius: 14px;
    width: 156px;
    margin: 29px 24px 0px 0px;
    padding: 4px 0px 4px 0px;
    opacity: 0.8;
    cursor: pointer;
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
