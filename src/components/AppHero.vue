<script>
import AppTitle from "./AppTitle.vue";

export default {
  data() {
    return {
      bgImageSrc: "../assets/img/0 JZqb4Omi99vifGH_.jpg",
    };
  },

  methods: {
    generateBackground(path) {
      const urlBg = new URL(path, import.meta.url);
      return urlBg.href;
    },
  },

  components: {
    AppTitle,
  },
};
</script>

<template>
  <div class="app-hero">
    <img :src="generateBackground(bgImageSrc)" alt="hero background" />
    <AppTitle></AppTitle>
  </div>
</template>

<style scoped>
.app-hero {
  position: relative;
  display: flex;
  align-items: flex-end;
  justify-content: center;
}

.app-hero img {
  border-radius: 50px;
}
</style>
