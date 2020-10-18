<template>
  <div class="seccion_preparacion">
    <div class="izq">
      <h2>
        <p>¿En qué consiste la</p>
        preparación en Talenty?
      </h2>
      <p>
        Talently es un programa enfocado en prepararte para que puedas afrontar
        exitosamente cualquier proceso de selección en desarrollo de software.
      </p>
      <p>
        Los contenidos te ayudan en una variedad de temas a lo largo del proceso
        de selección desde el ángulo de Carrrera, Técnico y de Inglés.
      </p>
    </div>
    <div class="der">
      <Tabs></Tabs>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="sass" scoped>
.seccion_preparacion
  color: $primary
  padding: 1em 5%
.izq
  h2
    font-size: 48px
    p
      font-size: 31.2px
      margin-bottom: 0
      line-height: 0
  p
    font-size: 16px
    margin-bottom: 1em
@media only screen and (min-width: 768px)
  .seccion_preparacion
    display: flex
    flex-direction: row
    justify-content: space-between
    align-items: center
    .izq
      width: 40%
    .der
      width: 55%
</style>
