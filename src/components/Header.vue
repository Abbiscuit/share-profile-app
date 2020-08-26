<template>
  <div id="nav">
    <router-link to="/">Home</router-link>|
    <router-link to="/about">About</router-link>|
    <router-link to="/profile">Profile</router-link>
  </div>
</template>

<script>
export default {
  name: "Header",
};
</script>

<style lang="scss" scoped>
#nav {
  padding: 16px;
  background-color: #fff;

  a {
    font-weight: bold;
    color: #2c3e50;
    display: inline-block;
    padding: 8px 16px;
    text-decoration: none;

    &.router-link-exact-active {
      color: #42b983;
      text-decoration: underline;
    }
  }
}
</style>