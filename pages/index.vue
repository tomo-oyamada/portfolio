<template lang="pug">
  .container
      h1.ttl Portfolio
</template>

<script>
import { mapGetters, mapActions } from "vuex";
export default {
  computed: {
    ...mapGetters({
      isLoading: "opening/isLoading"
    })
  },
  watch: {
    isLoading: async function(next, prev) {
      if (!next && prev) {
        // ここに好きなアニメーションとかの処理
        console.log("aaa");
      }
    }
  },
  mounted() {
    window.addEventListener("load", async () => {
      await this.$delay(1000); // PromiseでsetTimeOut返すプラグインです
      this.endLoding();
    });
  },
  methods: {
    ...mapActions({
      endLoding: "opening/endLoading"
    })
  }
};
</script>

<style lang="scss">
.container {
  max-width: 1200px;
  margin: rem(56) auto rem(56) auto;
  padding: 0 rem(16);
}

.title {
  position: fixed;
  top: 45%;
  left: 50%;
  // transform: translate(-50%, -50%);
  // font-family: "Petit Formal Script", cursive, "Playfair Display",
  //   "Noto Serif JP", serif;
  display: block;
  font-weight: 300;
  font-size: 50px;
  letter-spacing: 1px;
  // color: $c_white;
}
</style>
