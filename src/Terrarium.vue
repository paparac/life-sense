<template>
  <InfoButton />
  <Canvas />
</template>

<script lang="ts">
import { defineComponent } from "vue";
import Canvas from "@/views/Canvas.vue";
import InfoButton from "@/components/InfoButton.vue";

export default defineComponent({
  name: "Terrarium",
  components: { Canvas, InfoButton },
});
</script>

<style>
* {
  box-sizing: border-box;
}

html,
body {
  margin: 0;
  width: 100vw;
  height: 100vh;
}

#terrarium {
  --gap: 10px;
  --black: rgb(15, 15, 15);
  --white: whitesmoke;

  background: var(--black);
  color: var(--white);
  width: 100%;
  height: 100%;
  padding: var(--gap);
  display: flex;
  justify-content: center;
  align-items: center;
  position: relative;
}
</style>
