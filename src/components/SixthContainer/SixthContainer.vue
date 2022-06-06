<template class="main">
  <div class="container">
    <SixthInput
      @changeTitle="changeTitle"
      @changeDescription="changeDescription"
    />
    <TextBox :title="TitleValue" :description="DescriptionValue" />
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import SixthInput from "./SixthInput.vue";
import TextBox from "./TextBox.vue";

export default defineComponent({
  name: "SixthContainer",
  components: { SixthInput, TextBox },
  methods: {
    changeDescription: function (description: string) {
      this.DescriptionValue = description;
    },
    changeTitle(title: string) {
      this.TitleValue = title;
    },
  },
  data: () => ({
    TitleValue: "Title",
    DescriptionValue: "Description",
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
