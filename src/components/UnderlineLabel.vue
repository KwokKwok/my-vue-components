<template>
  <div class="underline-label">
    <label>
      <slot></slot>
    </label>
    <div class="line"></div>
  </div>
</template>

<script lang="ts">
import { Vue, Prop, Component } from "vue-property-decorator";
@Component
export default class UnderlineLabel extends Vue {}
</script>

<style lang="scss">
.underline-label {
  width: auto;
  display: inline-block;

  label {
    transition: 0.3s all ease-in-out;
  }

  .line {
    margin-top: 4px;
    background-color: blue;
    width: 0%;
    margin: 0 auto;
    height: 2px;
    transition: 0.3s all ease-in-out;
  }

  &:hover {
    label {
      color: blue;
    }
    .line {
      width: 100%;
    }
  }
}
</style>

