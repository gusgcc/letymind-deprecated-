<template>
  <div class="item">
    <input id="radio_item" type="checkbox" :name="Date.now()" />
    <label for="radio_item" class="item_title">
      <div><slot name="title">Track de Carrera</slot></div>
      <div class="icon">
        <img src="~/assets/svg/index/flecha.svg" alt="" role="button" />
      </div>
    </label>
    <div class="item_content">
      <slot name="content">
        Los contenidos del track de carrera están disñados para que domines
        cualquier proceso de selección, entender cómo funcionan, que debes
        esperarte en cada etapa, optimizar tu perfil profesional en todos los
        puntos de contacto que podría tener un reclutador contigo, negociación
        salarial, estrategias de entrevista, etc.
      </slot>
    </div>
  </div>
</template>

<script>
export default {
  name: "SPItem",
};
</script>

<style lang="sass" scoped>
.item
    width: 100%
    &_title
        width: 100%
        display: flex
        flex-direction: row
        justify-content: space-between
        padding: 1em 0
        font-size: 25px
        div
            display: inline-block
        .icon
          width: 30px
          height: 30px
          display: flex
          align-items: center
          justify-content: center
          border-radius: 50%
          background-color: #f9f4f9
          transition: ease 0.4s all
    &_content
        width: 100%
        max-height: 0px
        overflow: hidden
        transition: max-height 0.4s
    #radio_item
      display: none
    #radio_item:checked ~ &_content
      max-height: 500px
    #radio_item:checked ~ &_title .icon
      transform: rotate(180deg)
</style>
