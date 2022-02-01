<template>
<nav>
    <a href="#">About</a>
    <a href="#">Careers</a>
    <a href="#">Events</a>
    <a href="#">Products</a>
</nav>
</template>
<script>
export default {
    name: 'Navigation'
}
</script>
<style scoped>
nav{
    margin: 0 auto;
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
}

</style>