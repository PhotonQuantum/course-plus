<template>
  <div v-if="!ready">
    <transition name="fade">
      <div class="d-flex align-items-center">
        <div class="spinner-border spinner-border-sm mr-3 text-info"></div>
        <span class="text-info">正在加载数据……</span>
      </div>
    </transition>
  </div>
</template>

<script lang="ts">
import { Component, Vue, Prop } from "vue-property-decorator";

@Component
export default class Loading extends Vue {
  @Prop() private ready!: boolean;
}
</script>

<style scoped lang="scss"></style>
