<template>
  <div>
    <button @click="SubmitHandler">Toggle</button>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "SeventhInput",
  emits: ["toggleIsVisible"],
  data() {
    return {
      isVisible: true,
    };
  },
  methods: {
    SubmitHandler() {
      this.isVisible = !this.isVisible;
      this.$emit("toggleIsVisible", this.isVisible);
    },
  },
});
</script>
