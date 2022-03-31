<template>
  <div class="footer">
    <a class="link" href="">Instagram</a>
    <a class="link" href="">Contact</a>
  </div>
</template>

<script>
export default {};
</script>

<style>
.footer {
  background: red;
  position: fixed;
  bottom: 0;
  left: 0;
  padding: 0 50px 20px 50px;
  width: 100%;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  box-sizing: border-box;
  text-transform: uppercase;
}

.link {
  text-decoration: none;
  color: white;
  font-size: 14px;
  transition: transform 0.3s;
}
.link:hover {
  transform: translateX(10px);
}
</style>