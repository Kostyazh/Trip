<template>
  <div class="container">
    <img v-bind:src="element.images[0].path" alt="img" />
    <div class="found">
      <h1>
        {{element.category.title}}
        <span>$$$</span>
        <span class="flag">
          <svg
            width="15"
            height="15"
            viewBox="0 0 15 15"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              d="M7.64645 1.20117H2.22656V0.439453C2.22656 0.196758 2.0298 0 1.78711 0C1.54441 0 1.34766 0.196758 1.34766 0.439453V14.5605C1.34766 14.8032 1.54441 15 1.78711 15C2.0298 15 2.22656 14.8032 2.22656 14.5605V7.93945H7.64645C7.88915 7.93945 8.08591 7.7427 8.08591 7.5V1.64062C8.08591 1.39793 7.88915 1.20117 7.64645 1.20117Z"
              fill="#C7C7C7"
            />
            <path
              d="M13.621 8.80166L12.5144 6.03516L13.621 3.26865C13.6752 3.1333 13.6585 2.97979 13.5767 2.85908C13.495 2.73838 13.3588 2.66602 13.2129 2.66602H8.96484V7.5C8.96484 8.22686 8.37334 8.81836 7.64648 8.81836C6.98751 8.81836 6.40137 8.81836 5.74219 8.81836V8.96484C5.74219 9.20798 5.93903 9.4043 6.18164 9.4043H13.2129C13.3588 9.4043 13.495 9.33193 13.5767 9.21123C13.6585 9.09053 13.6752 8.93701 13.621 8.80166Z"
              fill="#C7C7C7"
            />
          </svg>
        </span>
      </h1>

      <!-- <p>{{element.description}}</p> -->
      <div id="app" class="p">
        <div v-html="vueHtml"></div>
      </div>

      <button>Read More</button>
      <div class="heart">
        <vue-star class="hart" animate="animated bounceIn" color="#F05654">
          <b slot="icon" class="fa fa-heart">&#10084;</b>
        </vue-star>
      </div>
      <!-- <label for="heart">
        <svg
          width="20"
          height="20"
          viewBox="0 0 20 20"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            d="M14.1695 0.929596C13.237 0.929596 12.3457 1.14337 11.5205 1.56502C10.9588 1.85199 10.4428 2.23327 10 2.68564C9.5572 2.23327 9.0412 1.85199 8.47946 1.56502C7.65423 1.14337 6.76297 0.929596 5.83043 0.929596C2.61555 0.929596 0 3.54514 0 6.76007C0 9.03714 1.2026 11.4556 3.57435 13.9483C5.55464 16.0296 7.97913 17.7645 9.66429 18.8534L10 19.0704L10.3357 18.8534C12.0209 17.7645 14.4454 16.0296 16.4257 13.9483C18.7974 11.4556 20 9.03714 20 6.76007C20 3.54514 17.3845 0.929596 14.1695 0.929596ZM15.5294 13.0955C13.7596 14.9555 11.6038 16.5368 10 17.5951C8.39616 16.5368 6.24037 14.9555 4.4706 13.0955C2.32499 10.8406 1.23711 8.70902 1.23711 6.76007C1.23711 4.22729 3.29769 2.16671 5.83047 2.16671C7.28866 2.16671 8.62817 2.83652 9.50544 4.00436L10 4.66271L10.4946 4.00436C11.3718 2.83652 12.7113 2.16671 14.1695 2.16671C16.7023 2.16671 18.7629 4.22729 18.7629 6.76007C18.7629 8.70902 17.675 10.8406 15.5294 13.0955Z"
            fill="#333333"
          />
        </svg>
      </label>-->
      <!-- <input id="hart" type="radio" /> -->
      <!-- <svg width="640" height="480" viewBox="0 0 640 480" xmlns="http://www.w3.org/2000/svg">
        <g id="layer1">
          <path
            id="svg_2"
            d="m219.28949,21.827393c-66.240005,0 -119.999954,53.76001 -119.999954,120c0,134.755524 135.933151,170.08728 228.562454,303.308044c87.574219,-132.403381 228.5625,-172.854584 228.5625,-303.308044c0,-66.23999 -53.759888,-120 -120,-120c-48.047913,0 -89.401611,28.370422 -108.5625,69.1875c-19.160797,-40.817078 -60.514496,-69.1875 -108.5625,-69.1875z"
          />
        </g>
      </svg>-->
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
  display: flex;
  justify-content: start;
  background-color: rgb(238, 238, 238);
  margin-top: 16px;

  .flag {
    cursor: pointer;
    float: right;
  }

  .found {
    width: 490px;
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
    width: 400px;
    height: 55px;
    margin: -7px 0px 0px 0px;
    overflow: hidden;
  }
  button {
    cursor: pointer;
    background-color: black;
    color: rgb(238, 238, 238);
    border: none;
    padding: 10px 50px 10px 50px;
    margin: 24px 30px 0px 0px;
  }
}
img {
  border: 1px solid slategray;
  height: 150px;
  width: 150px;
  background-color: rgb(238, 238, 238);
  margin: 25px 30px 40px 16px;
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
//heart 2
// svg {
//   display: block;
//   width: 50px;
//   height: auto;
// }

// #svg_2 {
//   fill: transparent;
//   stroke: #000;
//   stroke-width: 6px;
//   cursor: pointer;
//   transition: fill 0.3s;
// }
// #svg_2.filled {
//   fill: #000;
// }
.heart {
  display: block;
  margin-top: -70px;
  margin-left: 170px;
}
</style>