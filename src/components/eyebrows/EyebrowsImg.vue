<template>
    <div class="eyebrows_img">
        <img :src="selectedImg" :class="imgClass"/>
    </div>
</template>
<script>
export default {
  data() {
    return {
      selectedImg: require("../eyebrows/Angry.png"),
      imgClass: "eyebrows_img",
      images: [
        { src: require("../eyebrows/Angry.png"), class: "eyebrows_img" },
        { src: require("../eyebrows/Formed.png"), class: "eyebrows_img" },
        { src: require("../eyebrows/Round.png"), class: "eyebrows_img" },
        { src: require("../eyebrows/Thick.png"), class: "eyebrows_img" },
        { src: require("../eyebrows/Thin.png"), class: "eyebrows_img" },
        { src: require("../eyebrows/Unsure.png"), class: "eyebrows_img" },
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
.eyebrows_img {
  position: absolute;
  margin-top: -32px;
  background-repeat: no-repeat;
  background-position: center;
  top: 100px;
  margin-left: 108px;
  transform: translateX(-50%);
}
</style>