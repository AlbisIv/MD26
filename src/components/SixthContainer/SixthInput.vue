<template>
  <div>
    <input
      type="text"
      placeholder="Update title..."
      v-model="TitleValue"
      @change="SubmitTitleHandler"
    />

    <input
      type="text"
      placeholder="Update description..."
      v-model="DescriptionValue"
      @change="SubmitDescriptionHandler"
    />
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "SixthInput",
  emits: ["changeTitle", "changeDescription"],
  data() {
    return {
      TitleValue: "",
      DescriptionValue: "",
    };
  },
  methods: {
    SubmitDescriptionHandler: function () {
      this.$emit("changeDescription", this.DescriptionValue);

      this.DescriptionValue = "";
    },
    SubmitTitleHandler() {
      this.$emit("changeTitle", this.TitleValue);

      this.TitleValue = "";
    },
  },
});
</script>
