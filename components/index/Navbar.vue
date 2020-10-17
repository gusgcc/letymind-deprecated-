<template>
  <ul class="mi_navbar_md">
    <li class="logo"><a href="">Letymind</a></li>
    <button id="buttonHamburger" class="btn_hamburger_md" @click="toggleButton">
      <span class="arriba"></span>
      <span class="medio"></span>
      <span class="abajo"></span>
    </button>
    <div id="menu" class="menu">
      <div class="menu_inner">
        <li id="home" class="active"><a>Home</a></li>
        <li><a href="">Conoce el programa</a></li>
        <li><a href="">Historias de exito</a></li>
        <li><a href="">Preguntas frecuentes</a></li>
      </div>
    </div>
  </ul>
</template>
<script>
export default {
  data() {
    return {
      menuShow: true,
      hamburger: true,
    };
  },
  mounted() {
    window.addEventListener("resize", this.hamburgerSize);
  },
  beforeDestroy() {
    window.removeEventListener("resize", this.hamburgerSize);
  },
  methods: {
    hamburgerSize(e) {
      console.log("cambio hamburger", window.innerWidth);
      if (window.innerWidth >= 768) {
      } else {
        document.getElementById("menu").classList.remove("menu_show");
        document.getElementById("menu").classList.add("menu");
        document
          .getElementById("buttonHamburger")
          .classList.remove("btn_hamburger_md_active");
        document
          .getElementById("buttonHamburger")
          .classList.add("btn_hamburger_md");
      }
    },
    toggleButton(e) {
      if (document.getElementById("menu").classList.contains("menu_show")) {
        const buttonHamburger = document.getElementById("buttonHamburger");
        buttonHamburger.classList.remove("btn_hamburger_md_active");
        buttonHamburger.classList.add("btn_hamburger_md");
        const menu = document.getElementById("menu");
        menu.classList.remove("menu_show");
        menu.classList.add("menu");
      } else {
        document
          .getElementById("buttonHamburger")
          .classList.remove("btn_hamburger_md");
        document
          .getElementById("buttonHamburger")
          .classList.add("btn_hamburger_md_active");
        document.getElementById("menu").classList.remove("menu");

        document.getElementById("menu").classList.add("menu_show");
      }
    },
  },
};
</script>
<style lang="sass" scoped>
*
  transition: ease 0.4s all
li,a
  text-decoration: none
  list-style: none
  cursor: pointer
  color: $primary
.mi_navbar_md
  transition: ease 0.4s all
  font-size: 10px
li
  display: block
  cursor: pointer
  padding: 2em
li.active
  border-left: 0.5em solid #fa163f
  background-color: rgba(0,0,0,.03)
  font-weight: bold
  color: $primary_dark
a
  font-size: 2.4em
.mi_navbar_md
  width: 100%
  display: flex
  flex-direction: row
  flex-wrap: wrap
  justify-content: space-between
  align-items: center
  padding: 0 0.5em
.logo
  padding: 0
  font-size: 2em
.btn_hamburger_md
  border: none
  padding: 1em
  display: flex
  flex-direction: column
  justify-content: space-between
  span
    width: 3em
    display: block
  .arriba
    margin-bottom: 1em
    border-top: 0.2em solid
  .medio
    width: 2em

    border-top: 0.2em solid
  .abajo
    margin-top: 1em
    border-top: 0.2em solid
.btn_hamburger_md_active
  @extend .btn_hamburger_md
  .arriba
    width: calc( 3em * 1.4142 )
    transform: translate(0,1.2em) rotate(-45deg)
  .medio
    border-top: 0.2em solid
    opacity: 0
  .abajo
    width: calc( 3em * 1.4142 )
    transform: translate(0,-1.2em) rotate(225deg)
.menu
  width: 100%
  transition: max-height 0.4s
  max-height: 0px
  overflow: hidden
.menu_show
  width: 100%
  max-height: 500px

@media only screen and (min-width: 768px)
  .mi_navbar_md
    display: flex
    flex-direction: row
    justify-content: space-between
    padding: 4.8em 10%
    align-items: center
    flex-wrap: nowrap
  .btn_hamburger_md
    display: none
  .menu,.menu_show
    max-height: 50px
    display: inline
    width: auto
    .menu_inner
      display: inline
      #home
        display: none
  .logo
    font-size: 2em
  li
    padding: 0.5em 1em
    display: inline
  a
    font-size: 1.6em
    font-weight: 500
</style>
