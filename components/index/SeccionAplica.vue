<template>
  <div class="section_aplica">
    <h2>Nosotros solo ganamos</h2>
    <h1>si tú ganas primero</h1>
    <p>
      Nuestra principal fuente de ingresos se dá una vez que tú seas contratado,
      entonces nuestros esfuerzos están completamente alineados a que consigas
      el mejor salario posible.
    </p>
    <ButtonAplicaAhora class="btn-aply"></ButtonAplicaAhora>
  </div>
</template>

<script>
export default {};
</script>

<style lang="sass" scoped>
.section_aplica
  margin-top: 4em
  display: flex
  flex-direction: column
  align-items: center
  justify-content: center
  font-size: 10px
  color: white
  text-align: center
  background: url("~assets/img/bg-section.jpg") center center
  height: 350px
  h2
    font-size: 2.6em
    margin-bottom: 1em
  h1
    font-size: 4em
    font-weight: 800
    margin-bottom: 1em
  p
    display: none
@media only screen and (min-width: 768px)
  .btn-aply
    width: 30%
  .section_aplica
    p
      display: block
      padding: 0 15% 2em 15%
      font-size: 1.6em
</style>
