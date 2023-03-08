<template>
    <div class="mouth_img">
        <img :src="selectedImg" :class="imgClass"/>
    </div>
</template>
<script>
export default {
  data() {
    return {
      selectedImg: require("../mouth/Line.png"),
      imgClass: "mouth_img",
      images: [
        { src: require("../mouth/Line.png"), class: "mouth_img" },
        { src: require("../mouth/Beard_2.png"), class: "mouth_img" },
        { src: require("../mouth/Beard.png"), class: "mouth_img" },
        { src: require("../mouth/Lips.png"), class: "mouth_img" },
        { src: require("../mouth/Open_Smile.png"), class: "mouth_img" },
        { src: require("../mouth/Original.png"), class: "mouth_img" },
        { src: require("../mouth/Smile.png"), class: "mouth_img" },
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
.mouth_img {
    margin-left: -5px;
}
</style>