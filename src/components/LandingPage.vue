<template>
  <main class="pt-70px blue">
    <div id="home" class="mb-n1 blue pt-16 pt-sm-0">
      <!-- spacing hack -->
      <v-row class="py-6 py-sm-0"></v-row>
      <v-container class="mt-5">
        <v-row justify="space-between" class="mx-md-n8 mb-n16">
          <v-col cols="4" class="pa-0">
            <Cloud9
              type="light"
              style="position: relative"
              class="d-none d-sm-flex ml-sm-4 mt-n16"
            />
          </v-col>
          <v-col cols="4">
            <Cloud9
              type="light"
              style="position: relative"
              class="d-none d-sm-flex ml-sm-4 mt-1 pt-16"
            />
          </v-col>
        </v-row>
      </v-container>
      <v-container class="mt-n16">
        <v-row class="mt-n16 switchOnSmall">
          <v-col
            cols="5"
            offset="3"
            sm="3"
            offset-sm="2"
            class="mt-n16 d-flex align-content-end flex-column"
          >
            <Feliz
              alt="pinata"
              class="mt-5"
              style="max-height: 80vh; z-index: 1; position: relative"
            />
          </v-col>
          <v-col
            cols="8"
            offset="2"
            sm="4"
            offset-sm="0"
            class="text-center white--text"
          >
            <BostonHacksLogoTextShadowed
              class="mb-5"
              z-index="1"
              style="position: relative"
            />
            <h2>Y'all can't hack us!</h2>
            <v-btn
              rounded
              depressed
              x-large
              href="https://www.youtube.com/watch?v=dQw4w9WgXcQ"
              target="_blank"
              class="text-center ma-5"
              >Donate at your own risk</v-btn
            >
          </v-col>
        </v-row>
      </v-container>
      <Wave z-index="10" class="d-block" />
    </div>
  </main>
</template>

<script>
import Wave from "@/components/common/SVG/Wave";
import Cloud9 from "@/components/common/SVG/Cloud9";
import BostonHacksLogoTextShadowed from "@/components/common/SVG/BostonHacksLogoTextShadowed";
import Feliz from "@/components/common/SVG/Feliz";

export default {
  components: {
    Wave,
    Cloud9,
    BostonHacksLogoTextShadowed,
    Feliz,
  },
};
</script>

<style>
html {
  scroll-behavior: smooth;
}

@media only screen and (max-width: 600px) {
  .switchOnSmall {
    flex-direction: column-reverse;
  }
}
</style>
