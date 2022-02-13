<template>
  <section class="info-panel" v-show="isVisiblePanel">
    <h1 class="info-panel__title">Info:</h1>
    <div class="info-panel__content">
      <p>Red: 0</p>
      <p>Green: 0</p>
      <p>Blue: 0</p>
    </div>
  </section>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "InfoPanel",
  props: {
    isVisiblePanel: Boolean,
  },
});
</script>

<style scoped>
.info-panel {
  background: var(--black);
  border: 2px solid var(--white);
  border-radius: 30px;
  width: 50%;
  height: 50%;
  position: absolute;
  left: var(--gap);
  top: var(--gap);
  padding: var(--gap);
  padding-top: calc(var(--gap) * 3);
}

.info-panel__content {
  padding-top: var(--gap);
}
</style>
