<template>
  <div class="container">
    <BodyComp />
    <FooterComp />
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

import FooterComp from "./components/FooterComp.vue";
import BodyComp from "./components/BodyComp.vue";

export default defineComponent({
  name: "App",
  components: { BodyComp, FooterComp },
});
</script>

<style lang="scss">
@import "./assets/base.css";

#app {
  background-color: var(--color-background);
  width: 100vw;
  height: 100vh;
}

.container {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-between;
  width: 100%;
  height: 100%;
}
</style>
