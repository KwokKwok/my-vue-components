<template>
  <div class="home">
    <div class="prop-container">
      <underline-label>我是UnderlineLabel</underline-label>
      <arrow-tooltip>我是ArrowTooltip</arrow-tooltip>
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import UnderlineLabel from "@/components/UnderlineLabel.vue";
import ArrowTooltip from "@/components/ArrowTooltip.vue";

@Component({
  components: {
    UnderlineLabel,
    ArrowTooltip
  }
})
export default class Home extends Vue {}
</script>

<style lang="scss" scoped>
div + div {
  margin-top: 15px;
}
</style>
