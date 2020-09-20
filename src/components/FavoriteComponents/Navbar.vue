<template>
  <nav>
    <ul>
      <router-link tag="li" to="/" exact active-class="active">
        <a href="#">City guide</a>
      </router-link>
      <router-link tag="li" to="/Favorite" exact active-class="active">
        <a href="#">Favorite</a>
      </router-link>
    </ul>
  </nav>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
nav {
  background-color: rgb(238, 238, 238);
  width: 1000px;
  margin: 0;
  padding: 5px;
  ul {
    display: flex;
    justify-content: center;
    li {
      list-style: none;
      margin-right: 98px;
      a {
        font-size: 16px;
        text-decoration: none;
        color: black;
        opacity: 0.7;
      }
    }
  }
}
.active {
  border-bottom: 2px solid #000;
  opacity: 1;
  a {
    opacity: 1;
  }
}
</style>
