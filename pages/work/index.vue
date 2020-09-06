<template lang="pug">
  .container
    section#works
      h2.ttl Works
      p just sumples
      ul.works
        li.works-list
          nuxt-link(to="/work/noise1").works-link
            img.works-thumb(src="/img/thumb/work1.png" alt="#")
            p My First Fractal Noise
        li.works-list
          nuxt-link(to="/work/noise2").works-link
            img.works-thumb(src="/img/thumb/work2.png" alt="#")
            p My Second Fractal Noise
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.works {
  @include flex-style(space-between);
  flex-wrap: wrap;
  .works-list {
    width: 48%;
  }
  .works-link {
    display: block;
  }
  .works-thumb {
    width: 100%;
  }
}
</style>
