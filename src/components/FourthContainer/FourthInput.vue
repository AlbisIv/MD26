<template>
  <div>
    <input
      type="text"
      placeholder="blue"
      v-model="inputValue"
      @change="SubmitHandler"
    />
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "FourthInput",
  emits: ["changeColor"],
  data() {
    return {
      inputValue: "",
    };
  },
  methods: {
    SubmitHandler() {
      this.$emit("changeColor", this.inputValue);

      this.inputValue = "";
    },
  },
});
</script>
