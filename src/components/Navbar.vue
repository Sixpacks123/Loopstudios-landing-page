<template>
  <nav>
    <div class="font" v-if="name" id="logo">
      {{ name }}
    </div>
    <div v-else id="logo">
      <img v-bind:src="logoImg" alt="Logo" />
    </div>

    <ul class="nav-links">
      <li v-for="list in navLinks" :key="list.key">
        <a class="font" :href="list.link">{{ list.name }}</a>
      </li>
    </ul>

    <div v-on:click="openMobileNav()" id="burger">
      <div class="line1"></div>
      <div class="line2"></div>
      <div class="line3"></div>
    </div>
  </nav>
</template>

<script>
export default {
  name: 'Navbar',
  props: ['name', 'logoImg', 'navLinks'],
  methods: {
    openMobileNav() {
      const burger = document.getElementById('burger')
      const nav = document.querySelector('.nav-links')
      const navLinks = document.querySelectorAll('.nav-links li')
      // Toggle navigation on mobile
      nav.classList.toggle('nav-active')
      // Burger toggler
      burger.classList.toggle('toggle')
      // Animate navigation links
      navLinks.forEach((link, index) => {
        if (link.style.animation || link.style.webkitAnimation) {
          link.style.animation = ''
          link.style.webkitAnimation = ''
        } else {
          link.style.webkitAnimation = `navLinkFade 0.5s ease forwards ${
            index / 7
          }s`
          link.style.animation = `navLinkFade 0.5s ease forwards ${index / 7}s`
        }
      })
    }
  }
}
</script>

<style>
nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  min-height: 8vh;
}
div#logo {
  
  color: #fefefe;
  font-weight: 800;
  font-size: 2rem;
  z-index: 5;
}
ul.nav-links {
  display: flex;
  justify-content: flex-end;
  width: 40%;
  line-height: 75px;
}
ul.nav-links li {
  list-style: none;
}
ul.nav-links a {
  text-decoration: none;
  color: #fefefe;
  font-size: 1.2rem;
  font-weight: 500;
  display: block;
  padding: 10px 20px;
}
#burger {
  display: none;
  cursor: pointer;
}
#burger div {
  width: 30px;
  height: 3px;
  margin: 8px;
  background-color: #fefefe;
  transition: all 0.3s ease-in;
}

/* Tablet */
@media screen and (max-width: 1024px) {
  ul.nav-links {
    width: 50%;
  }
}
/* Mobile */
@media screen and (max-width: 768px) {
  ul.nav-links {
    position: absolute;
    flex-direction: column;
    width: 100%;
    height: 100vh;
    top:0;
    right: 0;
    padding: 100px;
    align-items: center;
    justify-content: flex-start;
    background-color: black;
    transform: translateX(100%);
    transition: transform 0.5s ease-in;
  }
  ul.nav-links li {
    opacity: 0;
  }
  ul.nav-links a {
    width: 100%;
  }
  div#burger {
    display: block;
  }
}
.nav-active {
  transform: translateX(0) !important;
}
@keyframes navLinkFade {
  from {
    opacity: 0;
    transform: translateX(-60px);
  }
  to {
    opacity: 1;
    transform: translateX(0px);
  }
}
.toggle .line1 {
  transform: rotate(-45deg) translate(-9px, 10px);
}
.toggle .line2 {
  opacity: 0;
}
.toggle .line3 {
  transform: rotate(45deg) translate(-5px, -6px);
}
</style>