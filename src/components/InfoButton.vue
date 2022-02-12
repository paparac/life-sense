<template>
  <button class="info-button">I</button>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "InfoButton",
});
</script>

<style scoped>
.info-button {
  --width: 30px;

  border: 2px solid var(--white);
  color: var(--white);
  background: transparent;
  font-weight: bold;
  border-radius: var(--width);
  width: var(--width);
  aspect-ratio: 1;
  cursor: pointer;
  user-select: none;
  transition: ease 0.2s;
  position: absolute;
  left: var(--gap);
  top: var(--gap);
}

.info-button:hover {
  transform: scale(1.1);
}

.info-button:active {
  transform: scale(0.9);
}
</style>
