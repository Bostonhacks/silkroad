<template>
  <v-app id="app">
    <router-view />
    <svg width="0" height="0">
      <filter
        id="basicDropShadow"
        x="-20%"
        y="-20%"
        width="140%"
        height="140%"
        filterUnits="objectBoundingBox"
        primitiveUnits="userSpaceOnUse"
        color-interpolation-filters="linearRGB"
      >
        <feOffset dx="2" dy="2" in="SourceAlpha" result="offset" />
        <feGaussianBlur stdDeviation="2 2" in="offset" result="blur" />
        <feFlood flood-color="#172841" flood-opacity="0.7" result="flood" />
        <feComposite in="flood" in2="blur" operator="in" result="composite" />
        <feMerge result="merge">
          <feMergeNode in="composite" result="mergeNode" />
          <feMergeNode in="SourceGraphic" result="mergeNode1" />
        </feMerge>
      </filter>
    </svg>
  </v-app>
</template>

<style>
html,
body {
  height: 100%;
}

#app {
  overflow-x: hidden;
  background-repeat: no-repeat;
  /* background-image: url("/assets/landingPage/bostonHacksLoadingLogo.svg"); */
  background-position: center calc(50vh - 75px);
  background-size: 150px;

  display: flex;
  flex-direction: column;
}

#router {
  flex: 1 0 auto;
}

.slide-enter-active,
.slide-leave-active {
  transition: opacity 0.5s, transform 0.5s;
}
.slide-enter,
.slide-leave-to {
  opacity: 0;
  transform: scale(0.97);
}

.pt-70px {
  padding-top: 70px;
}
</style>
