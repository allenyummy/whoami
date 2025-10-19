<template>
  <img
    class="icon"
    :alt="alt"
    :src="src"
    :width="size"
    :height="size"
    @click="onClickandGo(url)"
  />
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "IconItem",
  props: {
    alt: {
      type: String,
      default: "icon",
    },
    src: {
      type: String,
      required: true,
    },
    url: {
      type: String,
      default: "",
    },
    size: {
      type: [Number, String],
      default: 30,
    },
  },
  setup() {
    const onClickandGo = (url: string) => {
      window.open(url, "_blank");
    };

    return {
      onClickandGo,
    };
  },
});
</script>

<style scoped>
.icon:hover {
  cursor: pointer;
  transform: scale(1.1);
  transition: transform 0.1s;
}
</style>
