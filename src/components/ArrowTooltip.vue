<template>
  <div class="arrow-tooltip">
    <div class="content">
      <slot></slot>
    </div>
  </div>
</template>
<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
@Component
export default class ArrowTooltip extends Vue {}
</script>

<style lang="scss">
.arrow-tooltip {
  .content {
    position: relative;
    border: 1px solid rgba($color: #000000, $alpha: 0.1);
    border-radius: 3px;
    display: inline-block;
    background: wheat;
    padding: 0.5em;

    box-shadow: 0.2em 0.2em 1em 0 rgba(black, 0.15);

    &::before {
      content: "";
      position: absolute;
      top: -0.4em;
      left: 1em;

      /* 角标大小。0.4 * 4/5，勾股定理 */
      padding: 0.32em;

      /* 与框保持统一 */
      background: inherit;
      border: inherit;

      /* 去掉两个边框，然后旋转45度 */
      border-right: 0;
      border-bottom: 0;
      transform: rotate(45deg);
    }
  }
}
</style>
