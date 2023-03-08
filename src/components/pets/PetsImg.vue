<template>
    <div class="pets_img">
        <!-- <img src="../pets/Raptor.png"> -->
        <img src="../pets/Cat.png" v-show="toggle">
        <img src="../pets/Dog.png" v-show="toggle">
        <img src="../pets/Fish.png" v-show="toggle">
    </div>
</template>
<script>

</script>
<style>
.pets_img {
    margin-top: 20px;
    margin-left: -300px;
    transform: rotate(-20deg);
}
</style>