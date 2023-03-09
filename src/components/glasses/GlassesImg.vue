<template>
    <div class="glasses_img">
        <img :src="selectedImg" :class="imgClass"/>
    </div>
</template>
<script>
export default {
  data() {
    return {
      selectedImg: require("../glasses/Plain.png"),
      imgClass: "glasses_img",
      images: [
        { src: require("../glasses/Plain.png"), class: "glasses_img" },
        { src: require("../glasses/Reading.png"), class: "reading" },
        { src: require("../glasses/Sunnies.png"), class: "glasses_img" },
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
.glasses_img {
  position: absolute;
  margin-top: -23px;
  background-repeat: no-repeat;
  top: 100px;
  margin-left: 108px;
  transform: translateX(-50%);
  z-index: 1;
}
.reading {
  position: absolute;
  margin-top: -23px;
  background-repeat: no-repeat;
  top: 100px;
  width: 163px;
  margin-left: 108px;
  transform: translateX(-50%);
  z-index: 1;
}
</style>