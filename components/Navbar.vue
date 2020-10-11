<template>
  <ul class="mi_navbar_md">
    <li class="logo"><a href="">Letymind</a></li>
    <button
      class="btn_hamburger_md"
      @click="toggleButton"
      id="button_hamburger"
    >
      <span class="arriba"></span>
      <span class="medio"></span>
      <span class="abajo"></span>
    </button>
    <div
      id="menu"
      class="menu"
    >
      <li class="active"><a>Home</a></li>
      <li><a href="">Conoce el programa</a></li>
      <li><a href="">Historias de exito</a></li>
      <li><a href="">Preguntas frecuentes</a></li>
    </div>
  </ul>
</template>
<script>
export default {
  data () {
    return {
      menuShow: true,
      hamburger: true,
    }
  },
  mounted () {
    window.addEventListener('resize', this.hamburgerSize)
  },
  beforeDestroy () {
    window.removeEventListener('resize', this.hamburgerSize)
  },
  methods: {
    hamburgerSize (e) {
      console.log("cambio hamburger", window.innerWidth)
      if (window.innerWidth >= 768) {
      } else {
        document.getElementById('menu').classList.remove('menu_show')
        document.getElementById('menu').classList.add('menu')
        document.getElementById('button_hamburger').classList.remove('btn_hamburger_md_active')
        document.getElementById('button_hamburger').classList.add('btn_hamburger_md')
      }
    },
    toggleButton (e) {
      if (document.getElementById('menu').classList.contains('menu_show')) {
        document.getElementById('menu').classList.remove('menu_show')
        document.getElementById('menu').classList.add('menu')
        document.getElementById('button_hamburger').classList.remove('btn_hamburger_md_active')
        document.getElementById('button_hamburger').classList.add('btn_hamburger_md')
      } else {
        document.getElementById('menu').classList.remove('menu')
        document.getElementById('menu').classList.add('menu_show')
        document.getElementById('button_hamburger').classList.remove('btn_hamburger_md')
        document.getElementById('button_hamburger').classList.add('btn_hamburger_md_active')
      }
    },
  },
}
</script>
<style lang="sass" scoped>
*
  transition: all 0.4s
li,a
  text-decoration: none
  list-style: none
  cursor: pointer
  color: $primary
.mi_navbar_md
  font-size: 10px
@media only screen and (max-width: 499px)
  li
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
      width: calc( 3em * 1.4142 )
      transform: translate(0,1.2em) rotate(-45deg)
    .medio
      border-top: 0.2em solid
      opacity: 0
    .abajo
      width: calc( 3em * 1.4142 )
      margin-top: 1em
      border-top: 0.2em solid
      transform: translate(0,-1.2em) rotate(225deg)
  .menu
    width: 100%
    height: 0px
    overflow: hidden
    transition: ease 0.4s all
  .menu_show
    width: 100%
    height: auto
    transition: ease 0.4s all

@media only screen and (min-width: 500px)
  .mi_navbar_md
    display: flex
    flex-direction: row
    justify-content: space-between
    padding: 4.8em 10%
    align-items: center
  .btn_hamburger_md
    display: none
  .menu,.menu_show
    display: inline-flex
    width: auto
    height: auto
  .logo
    font-size: 2em
  li
    padding: 0.5em 1em
  a
    font-size: 1.6em
    font-weight: 500
  .menu
</style>
