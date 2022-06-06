<template class="main">
  <div class="container">
    <FourthInput @changeColor="changeColor" />
    <ColorBox :color="ColorContent" />
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import FourthInput from "./FourthInput.vue";
import ColorBox from "./ColorBox.vue";

export default defineComponent({
  name: "FourthContainer",
  components: { FourthInput, ColorBox },
  methods: {
    changeColor(color: string) {
      console.log(color);
      this.ColorContent = color;
    },
  },
  data: () => ({
    ColorContent: "",
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
