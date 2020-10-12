<template>
  <div class="info">
    <div class="izq">Tu mejor aliado para crecer <span> profesionalmente</span></div>
    <div class="der">
      Talently ha sido diseñado para ayudarte a conseguir el mejor trabajo
      posible, en cualquier parte del mundo. Estamos en esto juntos, desde tus
      primeros días en el programa hasta que consigas una oportunidad que te
      ofrezca crecimiento, nuevos retos y la flexibilidad que estás buscando.
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style scoped lang="sass">
.info
  width: 100%
  color: $primary
  font-size: 10px
.info
  margin-top: 5em
  padding: 0 2em
  .izq
    font-size: 2.6em
    span
      font-size: 4*10px
      font-weight: bold
  .der
    font-size: 1.6em
    margin-top: 2em
    background-color: rgba(0,0,0,.01)
    font-weight: 500
    border-left: 3px solid #9ea3ba
    margin-left: -20px
    margin-right: -20px
    padding: 20px
@media only screen and (min-width: 768px)
  .info
    padding: 0 10%

@media only screen and (min-width: 1059px)
  .info
    display: flex
    flex-direction: row
    align-items: center
    .izq
      width: 50%
      font-size: 3.12em
      span
        font-size: 4.8*10px
    .der
      margin-top: 0
      width: 50%
</style>
