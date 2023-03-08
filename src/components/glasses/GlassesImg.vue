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
        { src: require("../glasses/Reading.png"), class: "glasses_img" },
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
    margin-top: -18px;
    margin-left: -2px;
}
</style>