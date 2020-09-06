<template lang="pug">
  div
    Header
    Webgl
    transition(name="page")
      Nuxt
    Footer
</template>

<style lang="scss" scoped>
.page-enter-active {
  animation: zoomInDown 0.5s;
}
.page-leave-active {
  animation: zoomOutDown 0.5s;
}

// .page-enter,
// .page-leave-to {
//   opacity: 0;
// }
// .page-enter-active {
//   transition: all 1.5s;
// }

// .page-leave-active {
//   transition: all 1.5s;
// }

html {
  /* font-family: "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI",
    Roboto, "Helvetica Neue", Arial, sans-serif; */
  font-family: "Noto Serif JP", "Playfair Display", serif;
  line-height: 1.5;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
}
</style>

<script>
export default {
  transition: {
    name: "page",
    mode: ""
  },
  watch: {
    // routeが変わるときにシーンを変えるなどなにか処理する
    "$route.name": function(_new, _old) {}
  }
};
</script>
