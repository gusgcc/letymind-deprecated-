<template>
  <div class="acordeon_item">
    <input
      class="acordeon_item_radio"
      type="radio"
      name="acordeon_item"
      :id="name_item"
    />
    <label
      :for="name_item"
      class="acordeon_item_title"
    >

      <div>
        <svg
          width="16"
          height="14"
          viewBox="0 0 16 14"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            d="M2 6.1349L6.1349 10.2698L14.4047 2"
            stroke="#130BA4"
            stroke-width="3.88172"
          ></path>
        </svg>
        <slot name="title">Track de Carrera</slot>
      </div>
      <div class="icon">
        <img
          src="~/assets/svg/index/flecha.svg"
          alt=""
          role="button"
        />
      </div>
    </label>
    <div class="acordeon_item_content">
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
/* eslint-disable */
export default {
  data () {
    return {
      name_item: 'item_acordeon_' + Math.random() * 9999
    }
  },
};
</script>

<style lang="sass" scoped>
.acordeon_item
  width: 100%
  &_title
    width: 100%
    display: flex
    flex-direction: row
    justify-content: space-between
    padding: 1em 5%
    font-size: 25px
    cursor: pointer
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
    padding: 0 5%
    width: 100%
    max-height: 0px
    overflow: hidden
    transition: max-height 0.4s
  .acordeon_item_radio
    display: none
  .acordeon_item_radio:checked ~ &_content
    max-height: 500px
  .acordeon_item_radio:checked ~ &_title .icon
    transform: rotate(180deg)
</style>
