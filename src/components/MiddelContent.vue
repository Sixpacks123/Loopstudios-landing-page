<template>
    <div class="parent">
      <div class="child1">
          <img src="@/assets/img/desktop/image-interactive.jpg" alt="">
      </div>
      <div class="child1 child2"></div>
    </div>
</template>
<script>
export default {
    name: 'MiddelContent',
}
</script>
<style scoped>
.parent {
    position: relative;
    max-width: 100vh;
    height: 300px;
    margin: 10px;
}
.child1 {
    position: absolute;
    width: 70%;
    height: 100%;
    top: 0;
    left: 0;
    opacity: 0.7;
    background: red;
}
.child2 {
    z-index: 1;
    margin-left: 50%;
    margin-top: 200px;
    background: green;
}
</style>