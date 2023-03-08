<template>
    <div class="wrapper">
        <div class="frame">
            <BackgroundImg ref="backgroundImg"/>
            <BodysImg ref="bodysImg"/>
            <img src="../../src/components/Head.png" class="head">
            <TopImg ref="topImg"/>
            <EyebrowsImg ref="eyebrowsImg"/>
            <EyesImg ref="eyesImg"/>
            <GlassesImg ref="glassesImg"/>
            <MouthImg ref="mouthImg"/>
            <PetsImg ref="petsImg"/>
        </div>
    </div>
    <button class="btn" @click="random">СОЗДАТЬ</button>
</template>
<script>
import BackgroundImg from './backgrounds/BackgroundImg.vue';
import BodysImg from './bodys/BodysImg.vue';
import TopImg from './top/TopImg.vue';
import EyebrowsImg from './eyebrows/EyebrowsImg.vue';
import EyesImg from './eyes/EyesImg.vue';
import GlassesImg from './glasses/GlassesImg.vue';
import MouthImg from './mouth/MouthImg.vue';
import PetsImg from './pets/PetsImg.vue';
export default {
  components: {
        BackgroundImg,
        BodysImg,
        TopImg,
        EyebrowsImg,
        EyesImg,
        GlassesImg,
        MouthImg,
        PetsImg
    },
    data() {
    return {
        selectedImg: null,
        };
    },
    methods: {
    random() {
        this.$refs.backgroundImg.random();
        this.selectedImg = this.$refs.backgroundImg.selectedImg;
        this.$refs.bodysImg.random();
        this.selectedImg = this.$refs.bodysImg.selectedImg;
        this.$refs.eyebrowsImg.random();
        this.selectedImg = this.$refs.eyebrowsImg.selectedImg;
        this.$refs.eyesImg.random();
        this.selectedImg = this.$refs.eyesImg.selectedImg;
        this.$refs.glassesImg.random();
        this.selectedImg = this.$refs.glassesImg.selectedImg;
        this.$refs.mouthImg.random();
        this.selectedImg = this.$refs.mouthImg.selectedImg;
        this.$refs.petsImg.random();
        this.selectedImg = this.$refs.petsImg.selectedImg;
        this.$refs.topImg.random();
        this.selectedImg = this.$refs.topImg.selectedImg;
        },
    },
}
</script>
<style>
@font-face {
    font-family: 'RussoOne';
    src: url('../assets/RussoOne.ttf');
}
.wrapper {
    display: flex;
    justify-content: center;
    position: absolute;
    background-color: rgb(0, 0, 0);
    margin-top: -8px;
    margin-left: -8px;
    width: 100%;
    height: 100%;
}
.frame {
    position: relative;
    overflow: hidden;
    margin: 50px;
    width: 440px;
    height: 440px;
    border: 2px solid rgb(250, 250, 0);
    border-radius: 5px;
}
.btn {
    cursor: pointer;
    position: relative;
    margin-top: 500px;
    font-family: 'RussoOne';
    font-size: 25px;
    background-color: rgb(250, 250, 0);
    border-radius: 6px;
}
.btn:hover {
    transition: 0.2s;
    transform: scale(1.03);
    box-shadow: 1px 1px 25px 1px rgba(255, 0, 0);
}
.head {
    display: flex;
    margin-top: -389px;
    margin-left: 137px;
    height: 187px;
    width: 160px;
}
</style>