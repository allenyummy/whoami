<template>
  <div class="footer">
    <span>{{ footerDescription }}</span>
  </div>
</template>

<script lang="ts">
import {
  defineComponent,
  ref,
  computed,
  onMounted,
  onBeforeUnmount,
} from "vue";

export default defineComponent({
  name: "FooterComp",
  setup() {
    const screenWidth = ref(innerWidth);
    const onResize = () => {
      screenWidth.value = innerWidth;
    };
    const curYear = new Date().getFullYear();
    const footerDescription = computed(() => {
      return screenWidth.value < 420
        ? `Copyright © ${curYear} Yu-Lun Chiang \nAll rights reserved`
        : `Copyright © ${curYear} Yu-Lun Chiang. All rights reserved.`;
    });
    onMounted(() => {
      addEventListener("resize", onResize);
    });
    onBeforeUnmount(() => {
      removeEventListener("resize", onResize);
    });

    return {
      footerDescription,
    };
  },
});
</script>

<style scoped>
.footer {
  height: 5%;
  text-align: center;
  white-space: pre;
  margin: 0 0 1rem 0;
}
</style>
