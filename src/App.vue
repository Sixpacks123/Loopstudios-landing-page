<template>
  <div class="hero-image">
    <div class="page-container">
    <Header/>
    </div>
</div>
  <div class="page-container">
  </div>
</template>
<script>
import Header from './components/Header.vue'

export default {
  name: 'App',
  components:{
    Header
  }

}
</script>
<style >
*{
      margin: 0;
      padding: 0;
  }

html, body{
    height: auto;
  }

.hero-image {
  background-image: url("./assets/img/desktop/image-hero.jpg");
  height: 70%;
  width: 100%;
  top: 0;
    left: 0;
  background-repeat: no-repeat;
  background-size: cover;
  position: fixed;
}
.page-container { /** class for the same margin for all page */
   padding-top: 2em;
    max-width: 1400px;
    margin: 0 auto;
    
  }


  @media all and (max-width: 1200px){
    .page-container{
      max-width: 1200px;
      margin: 0 1.5em;
    }
  }

  @media all and (max-width: 900px){
    .page-container {
      padding: 1.5em 5px calc(70px + 1.5em) 5px;
    }
    .hero-image {
  background-image: url("./assets/img/mobile/image-hero.jpg");
  height: 100vh;
}
  }

</style>
