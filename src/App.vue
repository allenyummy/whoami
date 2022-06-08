<template>
  <div class="container">
    <div class="body">
      <img
        class="photo_sticker"
        alt="Photo Sticker"
        src="./assets/PhotoSticker.svg"
        width="150"
        height="150"
      />

      <div class="description">
        <span
          >I'm Yu-Lun Chiang. <br />Trying to be a reader and developer.</span
        >
      </div>

      <div class="icons">
        <img
          class="icon"
          alt="Github"
          src="./assets/iconmonstr-github-3.svg"
          width="30"
          height="30"
          @click="onClickandGo('https://github.com/allenyummy')"
        />
        <img
          class="icon"
          alt="Linkedin"
          src="./assets/iconmonstr-linkedin-3.svg"
          width="30"
          height="30"
          @click="
            onClickandGo('https://www.linkedin.com/in/yu-lun-chiang-37a070164/')
          "
        />
        <img
          class="icon"
          alt="Medium"
          src="./assets/iconmonstr-medium-3.svg"
          width="30"
          height="30"
          @click="onClickandGo('https://medium.com/@allenyummy')"
        />
      </div>
    </div>

    <div class="footer">
      <span>Copyright © {{ curYear }} Yu-Lun Chiang. All rights reserved.</span>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "App",
  setup() {
    const curYear = new Date().getFullYear();

    const onClickandGo = (url: string) => {
      window.open(url, "_blank");
    };

    return {
      curYear,
      onClickandGo,
    };
  },
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

  .body {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    width: 100%;
    height: 100%;

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

      .icon:hover {
        cursor: pointer;
        transform: scale(1.5);
        transition: transform 0.1s;
      }
    }
  }

  .footer {
    text-align: center;
    margin: 0 0 1rem 0;
  }
}
</style>
