<template>
    <div class="Top">
        <img src="../top/Cap.png" class="top_img" id="cap">
        <img src="../top/Bun.png" class="top_img" id="bun" v-show="toggle">
        <img src="../top/Crazy.png" class="top_img" id="crazy" v-show="toggle">
        <img src="../top/Curly.png" class="top_img" id="curly" v-show="toggle">
        <img src="../top/Long.png" class="top_img" id="long" v-show="toggle">
        <img src="../top/Mohawk.png" class="top_img" id="mohawk" v-show="toggle">
        <img src="../top/Mullet.png" class="top_img" id="mullet" v-show="toggle">
        <img src="../top/Ninja.png" class="top_img" id="ninja" v-show="toggle">
        <img src="../top/Ponytail.png" class="top_img" id="ponytail" v-show="toggle">
        <img src="../top/Smooth.png" class="top_img" id="smooth" v-show="toggle">
        <img src="../top/Styled.png" class="top_img" id="styled" v-show="toggle">
    </div>
</template>
<script>
export default {
    data() {
        return {
            images: [
                "Cap.png", "Bun.png", "Crazy.png", "Curly.png", "Long.png", "Mohawk.png", "Mullet.png", "Ninja.png", "Ponytail.png", "Smooth.png", "Styled.png"
            ]
        }
    },
    methods: {
        randomItem(items) {
            return items[Math.floor(Math.random()*items.length)]
        }
    },
    created() {
        this.selectedImage = this.randomItem(this.images)
    }
    // const allImg = [cap, bun, crazy, curly, long, mohawk, mullet, ninja, ponytail, smooth, styled]
    
    // const i = Math.trunc(Math.random() * allImg.length)
    // const o = document.createElement('img')
    // o.src = allImg[i]
    // document.querySelector('.Top').insertAdjacentElement('beforeend', o)
}
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