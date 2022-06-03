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
          >I'm Yu-Lun Chiang, <br />trying to be a reader and developer.</span
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

.logo {
  display: block;
  margin: 0 auto 2rem;
}

.container {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-between;
  width: 100%;
  height: 100%;

  .body {
    width: 100%;
    height: 100%;

    .photo_sticker {
      left: calc((100% - 150px) / 2);
      margin: 10rem 0 0 0;
      border: 6px solid var(--color-border-photo);
      border-radius: 100px;
    }

    .description {
      margin: 0.5rem 0;
      text-align: center;
    }

    .icons {
      display: flex;
      flex-direction: row;
      align-items: center;
      justify-content: center;
      gap: 20px;
      margin: 2em 0;

      .icon:hover {
        cursor: pointer;
      }
    }
  }

  .footer {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
    text-align: center;
    margin: 0 0 2rem 0;
  }
}

// a,
// .green {
//   text-decoration: none;
//   color: hsla(160, 100%, 37%, 1);
//   transition: 0.4s;
// }

// @media (hover: hover) {
//   a:hover {
//     background-color: hsla(160, 100%, 37%, 0.2);
//   }
// }

// @media (min-width: 1024px) {
//   body {
//     display: flex;
//     place-items: center;
//   }

//   #app {
//     display: grid;
//     grid-template-columns: 1fr 1fr;
//     padding: 0 2rem;
//   }

//   header {
//     display: flex;
//     place-items: center;
//     padding-right: calc(var(--section-gap) / 2);
//   }

//   header .wrapper {
//     display: flex;
//     place-items: flex-start;
//     flex-wrap: wrap;
//   }

//   .logo {
//     margin: 0 2rem 0 0;
//   }
// }
</style>
