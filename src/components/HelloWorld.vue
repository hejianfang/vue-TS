<template>
  <div class="hello">
    <h3>{{ msg }}</h3>
  </div>
</template>

<script lang="ts">
import {Prop, Component, Vue } from 'vue-property-decorator';
@Component
export default class HelloWorld extends Vue {
  @Prop({default: '123'}) private msg!: string;
}
</script>

<style scoped lang="less">
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
