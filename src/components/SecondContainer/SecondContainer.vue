<template class="main">
  <div class="container">
    <h3>{{ title }}</h3>
    <SecondInput v-model:title="title" />
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import SecondInput from "./SecondInput.vue";

export default defineComponent({
  name: "SecondContainer",
  components: { SecondInput },
  // methods: {
  //   changeTitle(title: string) {
  //     console.log(title);
  //     this.titleContent = title;
  //   },
  // },
  data: () => ({
    title: "Title",
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
