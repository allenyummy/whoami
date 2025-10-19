<template>
  <div class="body">
    <IconItem
      class="photo_sticker"
      alt="Photo Sticker"
      src="src/assets/PhotoSticker.svg"
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
    const icons = [
      {
        alt: "Github",
        src: "src/assets/iconmonstr-github-3.svg",
        url: "https://github.com/allenyummy",
        size: 30,
      },
      {
        alt: "LinkedIn",
        src: "src/assets/iconmonstr-linkedin-3.svg",
        url: "https://www.linkedin.com/in/yulun-chiang/",
        size: 30,
      },
      {
        alt: "Medium",
        src: "src/assets/iconmonstr-medium-3.svg",
        url: "https://medium.com/@allenyummy",
        size: 30,
      },
      {
        alt: "Gmail",
        src: "src/assets/iconmonstr-gmail-3.svg",
        url: "https://mail.google.com/mail/?view=cm&fs=1&tf=1&to=chiangyulun0914@gmail.com",
        size: 30,
      },
    ];

    const galleryItems = [
      {
        img: "src/assets/portfolio/referral-form-thumb.jpg",
        alt: "ReferralForm - Candidate Referral SaaS",
        href: "https://allenyummy.github.io/referral-form",
        title: "ReferralForm",
        desc: "Candidate referrals with hosted file uploads",
      },
      {
        img: "src/assets/portfolio/lust-studio-thumb.jpg",
        alt: "Lust Studio - Creative CMS",
        href: "https://allenyummy.github.io/lust-studio",
        title: "Lust Studio",
        desc: "CMS for creative production & curation",
      },
      {
        img: "src/assets/portfolio/lets-orgasm-thumb.jpg",
        alt: "Let's Orgasm! - E-commerce",
        href: "https://allenyummy.github.io/lets-orgasm",
        title: "Let's Orgasm!",
        desc: "Sex-positive curated e-commerce",
      },
      {
        img: "src/assets/portfolio/ai-notes-thumb.jpg",
        alt: "AI Notes - Meeting Summarizer",
        href: "https://allenyummy.github.io/ai-notes",
        title: "AI Notes",
        desc: "Record → transcribe → summarize",
      },
      {
        img: "src/assets/portfolio/ai-notes-thumb.jpg",
        alt: "AI Notes - Meeting Summarizer",
        href: "https://allenyummy.github.io/ai-notes",
        title: "AI Notes",
        desc: "Record → transcribe → summarize",
      },
      {
        img: "src/assets/portfolio/ai-notes-thumb.jpg",
        alt: "AI Notes - Meeting Summarizer",
        href: "https://allenyummy.github.io/ai-notes",
        title: "AI Notes",
        desc: "Record → transcribe → summarize",
      },
      {
        img: "src/assets/portfolio/ai-notes-thumb.jpg",
        alt: "AI Notes - Meeting Summarizer",
        href: "https://allenyummy.github.io/ai-notes",
        title: "AI Notes",
        desc: "Record → transcribe → summarize",
      },
      {
        img: "src/assets/portfolio/ai-notes-thumb.jpg",
        alt: "AI Notes - Meeting Summarizer",
        href: "https://allenyummy.github.io/ai-notes",
        title: "AI Notes",
        desc: "Record → transcribe → summarize",
      },
      {
        img: "src/assets/portfolio/ai-notes-thumb.jpg",
        alt: "AI Notes - Meeting Summarizer",
        href: "https://allenyummy.github.io/ai-notes",
        title: "AI Notes",
        desc: "Record → transcribe → summarize",
      },
      {
        img: "src/assets/portfolio/ai-notes-thumb.jpg",
        alt: "AI Notes - Meeting Summarizer",
        href: "https://allenyummy.github.io/ai-notes",
        title: "AI Notes",
        desc: "Record → transcribe → summarize",
      },
      {
        img: "src/assets/portfolio/ai-notes-thumb.jpg",
        alt: "AI Notes - Meeting Summarizer",
        href: "https://allenyummy.github.io/ai-notes",
        title: "AI Notes",
        desc: "Record → transcribe → summarize",
      },
    ];

    return {
      icons,
      galleryItems,
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
