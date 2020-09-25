<template lang="pug">
  .container
    section#works
      h2.ttl Works
      section.sec
        h3.subttl Website (need Password)
        p.website
          a.website-link(href="http://tomo-tsugu.sakura.ne.jp/portfolio/index.html" target="_blank" noopener noreferrer) Website Work
      section.sec
        h3.subttl WebGL shader art
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
.sec {
  margin-bottom: rem(48);
}
.website {
  .website-link {
    padding: rem(12) rem(16);
    border-radius: 4px;
    color: $c_black;
    background-color: $c_white;
    font-size: rem(16);
    -webkit-border-radius: 4px;
    -moz-border-radius: 4px;
    -ms-border-radius: 4px;
    -o-border-radius: 4px;
    transition: 0.2s;
    &:hover {
      background: $c_black;
      color: $c_white;
    }
  }
}
</style>
