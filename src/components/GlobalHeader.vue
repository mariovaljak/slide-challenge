<template>
  <div class="global-header">
    <div class="header-group-1">
      <img class="skull" src="../assets/Skull.png" />
      <img src="../assets/Group1233.svg" />
    </div>
    <div class="header-group-2">
      <div class="editors">
        <div class="line line-left"></div>
        editors
      </div>
      <div class="finish">
        <div class="line line-right"></div>
        finishing
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {};
  },
};
</script>

<style>
.global-header {
  background: red;
  position: fixed;
  top: 0;
  left: 0;
  z-index: 1;
  padding: 35px 50px 0 50px;
  width: 100%;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  box-sizing: border-box;
}
.header-group-1 {
  display: flex;
  flex-direction: row;
  justify-content: center;
}

.header-group-2 {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  text-transform: uppercase;
  font-size: 18px;
  cursor: pointer;
}

.line {
  border-bottom: 2px gray solid;
  width: 35px;
}

.line-left {
  margin-left: 25px;
  transform: translateX(5px);
}

.line-right {
  margin-right: 25px;
  transform: translateX(-5px);
}

.skull {
  margin-right: 20px;
}

.editors {
  display: flex;
  flex-direction: row-reverse;
  justify-content: center;
  align-items: center;
  transition: transform 0.3s;
}

.finish {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  transition: transform 0.3s;
}
.editors:hover {
  transform: translateX(-5px);
}

.editors:hover ~ .line-right {
  transform: translateX(0);
}

.finish:hover {
  transform: translateX(5px);
}

.finish:hover ~ .line-right {
  transform: translateX(0);
}
</style>