<template>
<nav>
    <a class="font" href="#">About</a>
    <a class="font" href="#">Careers</a>
    <a class="font" href="#">Events</a>
    <a class="font" href="#">Products</a>
    <a class="font" href="#">Supports</a>
</nav>
</template>
<script>
export default {
    name: 'Navigation'
}
</script>
<style scoped>
nav{
    position: relative;
    z-index: 2;
    pointer-events: none;
    display: flex;
    flex-direction: row;
    justify-content: flex-end;
}
a {
    pointer-events: initial;
    padding: 10px 20px;
    text-decoration: none;
    color: white;
    font-size: 15px;
}

</style>