<template>
  <div class="home">
    <underline-label>你好</underline-label>
    <button @click="go">测试</button>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import HelloWorld from "@/components/HelloWorld.vue"; // @ is an alias to /src
import UnderlineLabel from "@/components/UnderlineLabel.vue"; // @ is an alias to /src

@Component({
  components: {
    HelloWorld,
    UnderlineLabel
  }
})
export default class Home extends Vue {
  isActive: boolean = false;
  go() {
    this.isActive = !this.isActive;
  }
}
</script>

<style lang="scss" scoped>
.underline-label {
  margin: 10px;
}
</style>

