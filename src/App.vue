<template>
  <div class="page-container">
      <Header/>
    <div class="background">
        <img src="./assets/img/desktop/image-hero.jpg" alt="background" />
    </div>
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

 .background {
    height: 30vw;
    width: 100vw;
    top: 0;
    left: 0;
    position: fixed;
    background-color: black;
    z-index: -2;
    
  }
  img {
    height: 30vw;
      width: 100%;
      object-fit: cover;
      object-position: 50% 0;
    }
.page-container { /** class for the same margin for all page */
    width: 70%;
    height: auto;
    margin: 0 auto;
    background-color: red;
  }

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

</style>
