<template>
  <div>
    <input
      placeholder="Update title..."
      type="text"
      @input="$emit('update:title', $event.target.value)"
    />
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "SecondInput",
  props: ["title"],
  emits: ["update:title"],
  // data() {
  //   return {
  //     inputValue: "",
  //   };
  // },
  // methods: {
  //   SubmitHandler() {
  //     this.$emit("changeTitle", this.inputValue);

  //     this.inputValue = "";
  //   },
  // },
});
</script>
