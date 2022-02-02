<template>
    <div class="card ">
        <span class="font-text">IMMERSIVE</span>
        <span class="font-text">EXPERIENCES</span>
        <span class="font-text">THAT DELIVER</span>
    </div>
</template>
<script>
export default {
    name:'CardHero'
}
</script>
<style scoped>
.card{
    border: solid 1px white;
    display: flex;
    flex-direction: column;
    max-width: 700px;
    padding: 30px;
    align-items: flex-start;
    margin-top: 150px;
}
span{
    color: white;
    font-size: 4em;
    letter-spacing: 0.2em;
}
</style>