<template>
  <div class="container">
    <h1>Day {{element.day_order}}</h1>
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
};
</script>

<style lang="scss" scoped>
h1 {
  font-weight: 700;
  font-size: 20px;
  margin: 8px 0px 8px 0px;
}
</style>