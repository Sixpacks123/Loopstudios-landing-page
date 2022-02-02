<template>
<div>
    <div > 
    <Navbar
      name="loopstudios"
      :navLinks="[
        { name: 'About', link: '/about',},
        { name: 'Careers', link: '/about'},
        { name: 'Events', link: '/about'},
        { name: 'Products', link: '/about'},
        { name: 'Supports', link: '/about'}
      ]"
    /></div>
    <CardHero/>
</div>

</template>
<script>
import CardHero from '../components/CardHero.vue'
import Navbar from '../components/Navbar.vue'
export default {
    name : 'Header',
    components :{
        CardHero,
        Navbar
    }
}
</script>
<style scoped>

</style>