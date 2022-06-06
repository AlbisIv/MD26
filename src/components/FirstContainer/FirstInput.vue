<template>
  <div>
    <input type="text" placeholder="Update title..." v-model="inputValue" />
    <button @click="SubmitHandler">Change</button>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "FirstInput",
  emits: ["changeTitle"],
  data() {
    return {
      inputValue: "",
    };
  },
  methods: {
    SubmitHandler() {
      this.$emit("changeTitle", this.inputValue);

      this.inputValue = "";
    },
  },
});
</script>
<style scoped lang="scss">
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
