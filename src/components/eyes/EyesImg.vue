<template>
    <div class="eyes_img">
        <img :src="selectedImg" :class="imgClass"/>
    </div>
</template>
<script>
export default {
  data() {
    return {
      selectedImg: require("../eyes/Normal.png"),
      imgClass: "eyes_img",
      images: [
        { src: require("../eyes/Normal.png"), class: "eyes_img" },
        { src: require("../eyes/Lashes.png"), class: "eyes_img" },
        { src: require("../eyes/Nice.png"), class: "eyes_img" },
        { src: require("../eyes/Original.png"), class: "eyes_img" },
        { src: require("../eyes/Tired.png"), class: "eyes_img" },
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
.eyes_img {
  position: absolute;
  margin-top: -20px;
  background-repeat: no-repeat;
  background-position: center;
  z-index: 999;
  top: 100px;
  margin-left: 108px;
  transform: translateX(-50%);
}
</style>