<template>
  <div class="body">
    <IconItem
      class="photo_sticker"
      alt="Photo Sticker"
      :src="withBase('PhotoSticker.svg')"
      url="https://allenyummy.github.io/whoami/"
      size="100"
    />

    <div class="description">
      <span
        >I'm Yulun. <br />Being a reader and developer and delivering impacts on
        society.</span
      >
    </div>

    <div class="icons">
      <IconItem
        v-for="({ alt, src, url, size }, index) in icons"
        :key="index"
        :alt="alt"
        :src="src"
        :url="url"
        :size="size"
      />
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import IconItem from "./IconItem.vue";

export default defineComponent({
  name: "BodyComp",
  components: { IconItem },
  setup() {
    const withBase = (p: string) => import.meta.env.BASE_URL + p;

    const icons = [
      {
        alt: "Github",
        src: withBase("iconmonstr-github-3.svg"),
        url: "https://github.com/allenyummy",
        size: 30,
      },
      {
        alt: "LinkedIn",
        src: withBase("iconmonstr-linkedin-3.svg"),
        url: "https://www.linkedin.com/in/yulun-chiang/",
        size: 30,
      },
      {
        alt: "Medium",
        src: withBase("iconmonstr-medium-3.svg"),
        url: "https://medium.com/@allenyummy",
        size: 30,
      },
      {
        alt: "Gmail",
        src: withBase("iconmonstr-gmail-3.svg"),
        url: "https://mail.google.com/mail/?view=cm&fs=1&tf=1&to=chiangyulun0914@gmail.com",
        size: 30,
      },
    ];

    return {
      icons,
      withBase,
    };
  },
});
</script>

<style scoped>
.body {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  width: 100%;
  height: 95%;

  .photo_sticker {
    text-align: center;
    border: 6px solid var(--color-border);
    border-radius: 100px;

    &:hover {
      cursor: pointer;
      border: 7px solid var(--color-border-hover);
    }
  }

  .description {
    margin: 1rem 0;
    text-align: center;
  }

  .icons {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
    gap: 20px;
    margin: 1em 0;
  }
}
</style>
