<template class="main">
  <div class="container">
    <h3>{{ title }}</h3>
    <span>
      {{ description }}
    </span>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "TextBox",
  props: ["title" as string, "description" as string],
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
  flex-direction: column;
  border: 1px solid black;
  justify-content: center;
  align-items: center;
  max-width: 420px;
  width: 100%;
  min-height: 100px;
}
</style>
