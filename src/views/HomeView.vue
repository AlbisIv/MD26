<template>
  <div class="home">
    <FirstContainer />
    <SecondContainer />
    <ThirdContainer />
    <FourthContainer />
    <FifthContainer />
    <SixthContainer />
    <SeventhContainer />
    <EighthContainer />
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import FirstContainer from "@/components/FirstContainer/FirstContainer.vue"; // @ is an alias to /src
import SecondContainer from "@/components/SecondContainer/SecondContainer.vue";
import ThirdContainer from "@/components/ThirdContainer/ThirdContainer.vue";
import FourthContainer from "@/components/FourthContainer/FourthContainer.vue";
import FifthContainer from "@/components/FifthContainer/FifthContainer.vue";
import SixthContainer from "@/components/SixthContainer/SixthContainer.vue";
import SeventhContainer from "@/components/SeventhContainer/SeventhContainer.vue";
import EighthContainer from "@/components/EighthContainer/EighthContainer.vue";

export default defineComponent({
  name: "HomeView",
  components: {
    FirstContainer,
    SecondContainer,
    ThirdContainer,
    FourthContainer,
    FifthContainer,
    SixthContainer,
    SeventhContainer,
    EighthContainer,
  },
});
</script>

<style scoped lang="scss">
.home {
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
}
</style>
