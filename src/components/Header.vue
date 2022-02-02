<template>
<div>
    <div class="nav-content"> 
        <h1 class="font">loopstudios</h1>
        <Navigation/>
    </div>
    <CardHero/>
</div>

</template>
<script>
import CardHero from '../components/CardHero.vue'
import Navigation from '../components/Navigation.vue'
export default {
    name : 'Header',
    components :{
        CardHero,
        Navigation
    }
}
</script>
<style scoped>
.nav-content{
    display: flex;
    flex-direction: row;
    justify-content: space-between;
}

h1{
    color: hsl(0, 0%, 100%);
}
</style>