<template>
  <button class="btn_apply">APLICA AHORA <svg
      width="8"
      height="14"
      viewBox="0 0 8 14"
      fill="none"
      stroke="white"
      xmlns="http://www.w3.org/2000/svg"
    >
      <path
        d="M1 13L7 7L1 1"
        stroke-width="2"
        stroke-linecap="round"
        stroke-linejoin="round"
        class="icon-arrow"
      ></path>
    </svg></button>
</template>

<script>
export default {}
</script>

<style lang="sass" scoped>
button
  border: none
  outline: none
.btn_apply
  background: #FA163F
  color: white
  padding: 16.8px 48px
  font-size: 17.984px
  position: relative
  width: 85%
  font-weight: bold
  cursor: pointer
  &:before
    content: ""
    position: absolute
    transition: all .3s
    pointer-events: none
    transform-origin: top left
    right: -19px
    bottom: -19px
    width: 100%
    height: 100%
    border: 9px solid #12cad6
    border-top: 0
    border-left: 0
  svg
    position: absolute
    right: 20%
    transition: all .3s

  &:hover
    background: #e5052d
    svg
      position: absolute
      right: 15%
    &:before
      right: 0px
      bottom: 0px
</style>
