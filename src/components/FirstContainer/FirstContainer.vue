<template class="main">
  <div class="container">
    <h3>{{ titleContent }}</h3>
    <FirstInput @changeTitle="changeTitle" />
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import FirstInput from "./FirstInput.vue";

export default defineComponent({
  name: "FirstContainer",
  components: { FirstInput },
  methods: {
    changeTitle(title: string) {
      console.log(title);
      this.titleContent = title;
    },
  },
  data: () => ({
    titleContent: "Title",
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
