<template>
  <div class="background_img">
    <img :src="selectedImg" :class="imgClass" />
  </div>
</template>

<script>
export default {
  data() {
    return {
      selectedImg: require("../backgrounds/Boom.png"),
      imgClass: "background_imgs",
      images: [
        { src: require("../backgrounds/Boom.png"), class: "background_imgs" },
        { src: require("../backgrounds/Bricks.png"), class: "background_imgs" },
        { src: require("../backgrounds/Rectangle.png"), class: "background_imgs" },
      ],
    };
  },
  methods: {
    random() {
      const randIndex = Math.floor(Math.random() * this.images.length);
      this.selectedImg = this.images[randIndex].src;
      this.imgClass = this.images[randIndex].class;
    },
  },
};
</script>

<style>
.background_img {
  display: flex;
}

.background_imgs {
  width: 440px;
  height: 440px;
}
</style>