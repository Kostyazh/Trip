<template>
  <div class="container">
    <div class="heart">
      <vue-star class="hart" animate="animated bounceIn" color="#F05654">
        <b slot="icon" class="fa fa-heart">&#10084;</b>
      </vue-star>
    </div>
    <img
      v-bind:src="element.images[0].path"
      onerror="this.src='https://allauthor.com/img/20170730211046.png'"
      alt="img"
    />
    <div class="found">
      <h1>
        {{element.category.title}}
        <span>$$$</span>
      </h1>
      <div id="app" class="p">
        <div v-html="vueHtml"></div>
      </div>
    </div>
  </div>
</template>

<script>
import VueStar from "vue-star";
export default {
  components: {
    VueStar,
  },
  props: {
    element: {
      type: Object,
      required: true,
    },
  },
  data: function () {
    return {
      vueHtml: this.element.description,
    };
  },
};
</script>

<style lang="scss" scoped>
.container {
  width: 320px;
  height: 330px;
  margin-top: 16px;

  .flag {
    cursor: pointer;
    float: right;
  }

  .found {
    width: 290px;
    margin: 20px 0px 20px 0px;
  }
  h1 {
    font-size: 20px;
    text-transform: uppercase;
  }
  span {
    margin-left: 22px;
    font-size: 17px;
  }
  .p {
    width: 320px;
    height: 72px;
    margin: -25px 0px 0px 0px;
    overflow: hidden;
  }
}
img {
  width: 320px;
  height: 190px;
  object-fit: cover;
  background-color: rgb(238, 238, 238);
}
label {
  cursor: pointer;
}
input:checked {
  background-color: #000;
}

input[type="checkbox"] {
  width: 15px;
  height: 15px;
  border-radius: 50%;
  margin: -10;
  padding: 0;
  -moz-appearance: none;
  -webkit-appearance: none;
  -ms-appearance: none;
  -o-appearance: none;
  appearance: none;
  outline: none;
}
.heart {
  display: block;
  margin-top: -10px;
  margin-left: 240px;
}
.VueStar {
  margin-top: -28px;
}
b {
  cursor: pointer;
}
</style>