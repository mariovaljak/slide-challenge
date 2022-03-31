<template>
  <div class="block">
    <img class="image" :src="image" alt="" />
    <div class="meta">
      <h2 class="name">{{ name }}</h2>
      <h3 class="work-name">{{ workName }}</h3>
      <span class="button"
        ><img class="play-button" src="../assets/playButton.svg" alt="" />
        play</span
      >
    </div>
  </div>
</template>

<script>
export default {
  props: {
    name: {
      type: String,
      default: "",
    },
    image: {
      type: String,
      default: "",
    },
    workName: {
      type: String,
      default: "",
    },
  },
};
</script>

<style>
.block {
  position: relative;
}

.image {
  width: 100%;
  height: 100vh;
  object-fit: cover;
  object-position: center;
  display: block;
  z-index: -1;
}

.meta {
  position: absolute;
  top: 50%;
  left: 50%;
  text-align: center;
  transform: translate(-50%, -50%);
}

.name {
  font-size: 76px;
  margin: 0;
  transition: transform 0.3s;
}

.work-name {
  font-size: 28px;
  margin: 0;
  margin-bottom: 15px;
  transition: transform 0.3s;
}

.button {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  font-size: 18px;
  text-transform: uppercase;
  opacity: 0;
  transition: transform 0.3s, opacity 0.3s;
}

.play-button {
  height: 18px;
  width: auto;
  margin-right: 10px;
}
</style>