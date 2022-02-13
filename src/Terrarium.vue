<template>
  <InfoButton
    :isVisiblePanel="isVisiblePanel"
    :changeVisiblePanel="changeVisiblePanel"
  />
  <InfoPanel :isVisiblePanel="isVisiblePanel" />
  <Canvas />
</template>

<script lang="ts">
import { defineComponent, ref } from "vue";

import Canvas from "@/views/Canvas.vue";
import InfoButton from "@/components/InfoButton.vue";
import InfoPanel from "@/components/InfoPanel.vue";

export default defineComponent({
  name: "Terrarium",
  components: { Canvas, InfoButton, InfoPanel },

  setup() {
    let isVisiblePanel = ref(false);

    function changeVisiblePanel(): void {
      isVisiblePanel.value = !isVisiblePanel.value;
    }

    return {
      isVisiblePanel,
      changeVisiblePanel,
    };
  },
});
</script>

<style>
@font-face {
  font-family: "Fira Code";
  src: url("/FiraCode.ttf") format("truetype-variations");
  font-weight: 100 900;
  font-display: fallback;
}

:root {
  --gap: 10px;
  --black: #141414;
  --white: #f3f3f3;
  --trasition: ease 0.2s;
}

* {
  box-sizing: border-box;
  font-family: "Fira Code", monospace;
}

*::selection {
  background: var(--white);
  color: var(--black);
}

html,
body {
  margin: 0;
  width: 100vw;
  height: 100vh;
}

h1,
h2,
h3,
h4,
h5,
h6,
p {
  margin: 0;
}

#terrarium {
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
