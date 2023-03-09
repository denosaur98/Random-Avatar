<template>
  <div class="tops">
    <div :class="'top ' + selectedImg"></div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      selectedImg: 'cap',
      images: [
        'cap',
        'bun',
        'crazy',
        'curly',
        'long',
        'mohawk',
        'mullet',
        'ninja',
        'ponytail',
        'smooth',
        'styled'
      ]
    };
  },
  methods: {
    random() {
      const randIndex = Math.floor(Math.random() * this.images.length);
      this.selectedImg = this.images[randIndex];
    }
  }
};
</script>

<style>
.tops {
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  z-index: 2;
}

.top {
  background-repeat: no-repeat;
  background-size: cover;
  margin: 30px;
  z-index: 2;
}

.cap {
  background-image: url('../top/Cap.png');
  margin-top: -300px;
  width: 258px;
  height: 225px;
}

.bun {
  background-image: url('../top/Bun.png');
  margin-top: -285px;
  width: 258px;
  height: 230px;
}

.crazy {
  background-image: url('../top/Crazy.png');
  margin-top: -260px;
  width: 258px;
  height: 225px;
}

.curly {
  background-image: url('../top/Curly.png');
  margin-top: -265px;
  width: 258px;
  height: 225px;
}

.long {
  background-image: url('../top/Long.png');
  margin-top: -255px;
  width: 258px;
  height: 342px;
}

.mohawk {
  background-image: url('../top/Mohawk.png');
  margin-top: -275px;
  margin-right: 38px;
  width: 258px;
  height: 244px;
}

.mullet {
  background-image: url('../top/Mullet.png');
  margin-top: -255px;
  width: 258px;
  height: 246px;
}

.ninja {
  background-image: url('../top/Ninja.png');
  margin-top: -280px;
  width: 258px;
  height: 225px;
}

.ponytail {
  background-image: url('../top/Ponytail.png');
  margin-top: -260px;
  width: 258px;
  height: 228px;
}

.smooth {
  background-image: url('../top/Smooth.png');
  margin-top: -265px;
  width: 258px;
  height: 231px;
}

.styled {
  background-image: url('../top/Styled.png');
  margin-top: -265px;
  width: 258px;
  height: 225px;
}
</style>