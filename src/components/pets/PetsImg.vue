<template>
    <div class="pets_img">
        <img :src="selectedImg" :class="imgClass"/>
    </div>
</template>
<script>
export default {
  data() {
    return {
      selectedImg: require("../pets/Raptor.png"),
      imgClass: "pets_img",
      images: [
        { src: require("../pets/Raptor.png"), class: "pets_img" },
        { src: require("../pets/Cat.png"), class: "pets_img cat" },
        { src: require("../pets/Dog.png"), class: "pets_img dog" },
        { src: require("../pets/Fish.png"), class: "pets_img" },
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
.pets_img {
  position: absolute;
  background-repeat: no-repeat;
  top: 150px;
  margin-left: -25px;
  z-index: 2;
}
.cat, .dog {
  top: 120px;
}
</style>