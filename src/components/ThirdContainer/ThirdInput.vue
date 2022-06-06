<template>
  <div>
    <input type="text" placeholder="blue" v-model="inputValue" />
    <button @click="SubmitHandler">Change</button>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "ThirdInput",
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
