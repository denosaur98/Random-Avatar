<template>
    <div class="Top">
        <img :src="selectedImg" :class="imgClass"/>
    </div>
</template>
<script>
export default {
  data() {
    return {
      selectedImg: require("../top/Cap.png"),
      imgClass: "top_img",
      images: [
        { src: require("../top/Cap.png"), class: "top_img" },
        { src: require("../top/Bun.png"), class: "top_img" },
        { src: require("../top/Crazy.png"), class: "top_img" },
        { src: require("../top/Curly.png"), class: "top_img" },
        { src: require("../top/Long.png"), class: "top_img" },
        { src: require("../top/Mohawk.png"), class: "top_img" },
        { src: require("../top/Mullet.png"), class: "top_img" },
        { src: require("../top/Ninja.png"), class: "top_img" },
        { src: require("../top/Ponytail.png"), class: "top_img" },
        { src: require("../top/Smooth.png"), class: "top_img" },
        { src: require("../top/Styled.png"), class: "top_img" },
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
.top_img {
    display: flex;
    margin-top: -270px;
    margin-left: 91px;
    Width: 257px;
    height: 225px;
}
</style>