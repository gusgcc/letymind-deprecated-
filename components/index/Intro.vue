<template>
  <div class="intro">
    <div class="izq">
      <h1>Consigue un trabajo remoto que multiplique tu salario!</h1>
      <p>
        Te preparamos para que puedas afrontar los más rigurosos procesos de
        selección y te conectamos con empresas de todo el mundo que buscan
        talento como el tuyo.
      </p>
      <ButtonAplicaAhora></ButtonAplicaAhora>
      <p>Últimos dias para aplicar</p>
    </div>
    <div class="der">
      <svgintromarketing
        width="100%"
        height="auto"
      > </svgintromarketing>
      <div class="item_card">
        <h4>USD <span>45K</span></h4>
        <span>Salario anual promedio de nuestros egresados</span>
      </div>
    </div>
  </div>
</template>

<script>
import svgintromarketing from "~/assets/svg/index/intro-marketing.svg?inline"
export default {
  components: {
    svgintromarketing
  }
}
</script>

<style lang="sass" scoped>
*
  transition: all 0.4s
.intro
  font-size: 10px
.intro
  margin-top: 1em
  .izq
    padding: 0 2em
    h1
      font-size: 4em
      color: $primary
      font-weight: bold
      line-height: 1
    p
      margin: 2.4em 0
      font-size: 1.6em
      color: $primary
  .der
@media only screen and (min-width: 768px)
  .intro
    padding: 0 10%

@media only screen and (min-width: 1059px)
  .intro
    padding: 0
    display: flex
    flex-direction: row
    align-items: center
    .izq,.der
      width: 50%
      h1
        font-size: 4.8em
        font-weight: 800
      p
        margin-right: 15%
      button
        width: 50%
    .izq
      padding: 0 5%
</style>
