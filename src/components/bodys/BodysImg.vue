<template>
    <div class="bodys">
      <img src="../bodys/Muscle_shirt.png" class="muscle">
    </div>
</template>
<script>
export default {
data() {
    return {
        selectedImg: null,
        toggle: false,
    };
},
methods: {
    random() {
        const images = [
            {src: require("../bodys/Muscle_shirt.png"), classList: "muscle"},
            {src: require("../bodys/Necklace.png"), classList: "necklace"},
            {src: require("../bodys/Plain.png"), classList: "plain"},
            {src: require("../bodys/Print.png"), classList: "print"},
            {src: require("../bodys/Super_hero.png"), classList: "superhero"},
            {src: require("../bodys/Sweater.png"), classList: "sweater"},
        ];
        const firstImg = document.querySelector(".bodys img");
        const randIndex = Math.floor(Math.random() * images.length);
        firstImg.src = images[randIndex].src;
        firstImg.classList = "bodys " + images[randIndex].classList;
        },
    }
};
</script>
<style>
.bodys {
    display: flex;
}
.muscle {
    display: flex;
    margin-top: -169px;
    margin-left: 70px;
    width: 295px;
    height: 223px;
}
.necklace {
    display: flex;
    margin-top: -162px;
    margin-left: 70px;
    width: 295px;
    height: 216px;
}
.plain {
    display: flex;
    margin-top: -162px;
    margin-left: 70px;
    width: 295px;
    height: 216px;
}
.print {
    display: flex;
    margin-top: -162px;
    margin-left: 70px;
    width: 295px;
    height: 216px;
}
.superhero {
    display: flex;
    justify-content: center;
    margin-top: -169px;
    margin-left: 47px;
    width: 336px;
    height: 223px;
}
.sweater {
    display: flex;
    margin-top: -163px;
    margin-left: 70px;
    width: 295px;
    height: 217px;
}
</style>