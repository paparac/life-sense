<template>
  <div class="info-panel">
    <h2>Info</h2>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "InfoPanel",
});
</script>

<style scoped>
.info-panel {
  border: 2px solid var(--white);
}
</style>
