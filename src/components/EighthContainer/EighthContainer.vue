<template class="main">
  <div class="container">
    <EighthInput @toggleIsVisible="changeColor" />
    <ColorBox :isVisible="isVisible" />
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import EighthInput from "./EighthInput.vue";
import ColorBox from "./ColorBox.vue";

export default defineComponent({
  name: "EighthContainer",
  components: { EighthInput, ColorBox },
  methods: {
    changeColor(isVisible: boolean) {
      console.log(isVisible);
      this.isVisible = isVisible;
    },
  },
  data: () => ({
    isVisible: true,
  }),
});
</script>
<style scoped lang="scss">
.container {
  display: flex;
  border: 1px solid black;
  justify-content: center;
  align-items: center;
  max-width: 420px;
  width: 100%;
  min-height: 100px;
}
</style>
