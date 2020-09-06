<template lang="pug">
  .container
    section#works-detail
      .sample
        video(alt="ノイズ１" autoplay muted playinline loop)
          source(src="/video/work2.mov" type="video/mp4")
          p My First Fractal Noise
      .intro
        h2.ttl.mod-mid ノイズその2
        p fragmentで頑張りました
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
