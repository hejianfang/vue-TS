<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <HelloWorld :msg="msg"/>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import HelloWorld from '@/components/HelloWorld.vue'; // @ is an alias to /src

@Component({
  components: { HelloWorld },
})
export default class Home extends Vue {
  private msg: string = '你好哦';
  private created() {
    console.log(this.msg);
  }
}
</script>
