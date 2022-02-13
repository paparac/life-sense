<template>
  <div id="dom-layout">
    <InfoButton
      :isVisiblePanel="isVisiblePanel"
      :changeVisiblePanel="changeVisiblePanel"
    />
    <InfoPanel :isVisiblePanel="isVisiblePanel" />
  </div>
</template>

<script lang="ts">
import { defineComponent, ref } from "vue";
import InfoButton from "@/components/InfoButton.vue";
import InfoPanel from "@/components/InfoPanel.vue";

export default defineComponent({
  name: "DomLayout",

  components: { InfoButton, InfoPanel },

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

<style scoped>
#dom-layout {
  width: 100%;
  height: 100%;
  position: absolute;
}
</style>
