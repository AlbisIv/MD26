<template class="main">
  <div :style="{ 'background-color': color }" class="container"></div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "ColorBox",
  props: ["color" as string],
  methods: {
    // changeTitle(title: string) {
    //   console.log(title);
    //   this.titleContent = title;
    // },
  },
  data: () => ({
    // titleContent: "Title",
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
