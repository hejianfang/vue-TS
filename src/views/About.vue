<template>
  <div class="about">
    <h1>This is an about page</h1>
    <HelloWorld :msg='msg'/>
  </div>
</template>
<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import HelloWorld from '@/components/HelloWorld.vue'; // @ is an alias to /src

@Component({
  components: { HelloWorld },
})
export default class Home extends Vue {
  private msg: string = '你好 TS';
  private created() {
    console.log(this.msg);
  }
}
</script>