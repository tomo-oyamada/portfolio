<template lang="pug">
  .container
    section#works-detail
      .intro
        h2.ttl.mod-mid Noise1
        p First sample
      .sample
        video(alt="ノイズ１" autoplay muted loop playinline)
          source(src="/video/work1.mov" type="video/mp4")
          p My First Fractal Noise
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
#works-detail {
  padding: rem(10);
  background-color: $c_backBlack;
  .sample {
    width: 70%;
    margin: rem(20) auto;
    opacity: 1;
  }
  .intro {
    h2 {
      // padding-left: rem(16);
      // border-left: 6px solid $c_white;
    }
  }
}
</style>
