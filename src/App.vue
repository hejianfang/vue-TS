<template>
  <div id="app">
    <div id="nav">
      <a @click="handleClick('/')">Home</a> |
      <a @click="handleClick('/about')">About</a>
    </div>
    <router-view/>
  </div>
</template>
<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
@Component
export default class Home extends Vue {
  private handleClick(path: string): void {
    this.$router.push(path);
  }
}
</script>
<style lang="less">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
#nav {
  padding: 30px;
  a {
    font-weight: bold;
    color: #2c3e50;
    cursor: pointer;
    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
