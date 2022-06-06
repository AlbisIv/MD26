<template>
  <div>
    <input type="checkbox" model="isVisible" :onchange="SubmitHandler" />
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "EighthInput",
  emits: ["toggleIsVisible"],
  data() {
    return {
      isVisible: false,
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
