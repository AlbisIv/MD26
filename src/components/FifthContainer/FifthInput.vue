<template>
  <div>
    <input type="text" placeholder="Update title..." v-model="TitleValue" />
    <button @click="SubmitTitleHandler">Change</button>
    <input
      type="text"
      placeholder="Update description..."
      v-model="DescriptionValue"
    />
    <button @click="SubmitDescriptionHandler">Change</button>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "FifthInput",
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
