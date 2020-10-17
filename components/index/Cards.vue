<template>
  <div class="container_cards">
    <Card>
      <template v-slot:icon>
        <svg
          width="58"
          height="56"
          viewBox="0 0 58 56"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            d="M28.5907 11.224L35.3251 0L44.3042 9.42814L28.5907 11.224Z"
            fill="#5BBFCC"
          ></path>
          <path
            d="M37.1209 44.8995L43.4099 51.1886L55.988 38.6105"
            stroke="#5BBFCC"
            stroke-width="5.45049"
          ></path>
          <circle
            cx="11.9792"
            cy="17.9584"
            r="8.97918"
            stroke="#5BBFCC"
            stroke-width="5.45049"
          ></circle>
          <rect
            x="11.9792"
            y="16.1625"
            width="34.1209"
            height="24.2438"
            fill="#5BBFCC"
            style="mix-blend-mode: multiply"
          ></rect>
          <path
            d="M4.79584 49.3855C15.1219 47.7393 39.8147 36.8146 36.6719 10.326"
            stroke="#5BBFCC"
            stroke-width="5.38751"
            style="mix-blend-mode: multiply"
          ></path>
        </svg>
      </template>
      <template v-slot:title> Track Técnico </template>
      <template v-slot:detail>
        Vuélvete un experto en algoritmos y estructuras de datos para superar
        tus entrevistas técnicas, mejorar tu performance en tests de código y
        entregar “take-home-challenges" de calidad.
      </template>
    </Card>
    <Card>
      <template v-slot:icon>
        <svg
          width="51"
          height="50"
          viewBox="0 0 51 50"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            d="M0 40.4077V0H41.1923V30.9923H9.41538L0 40.4077Z"
            fill="#F6C55B"
            fill-opacity="0.6"
          ></path>
          <path
            d="M51 49.8231V23.9308H25.1077V43.7899H45.0818L51 49.8231Z"
            fill="#F6C55B"
            style="mix-blend-mode: multiply"
          ></path>
          <g style="mix-blend-mode: multiply">
            <path
              d="M11.7692 14.1231L17.2615 19.6154L28.2461 8.63077"
              stroke="#F6C55B"
              stroke-width="5.35288"
            ></path>
          </g>
        </svg>
      </template>
      <template v-slot:title> Track de Carrera </template>
      <template v-slot:detail>
        Contarás con un mentor personal que te acompañara a navegar tus procesos
        de seleccion y una curricula rigurosa que te permititra desarrollar tu
        marca personal y destacar en el mercado profesional.
      </template>
    </Card>
    <Card>
      <template v-slot:icon>
        <svg
          width="55"
          height="55"
          viewBox="0 0 55 55"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <rect
            x="26.1904"
            y="16.1509"
            width="28.8095"
            height="24.4444"
            fill="#82C68F"
            style="opacity: 0.8"
          ></rect>
          <g style="mix-blend-mode: multiply; opacity: 0.6">
            <rect
              x="11.3496"
              y="30.1191"
              width="28.8095"
              height="24.4444"
              fill="#82C68F"
            ></rect>
          </g>
          <path
            d="M3.92857 28.373L0 24.0079L19 5.03174L15.7143 1.74603L28.373 0L26.627 11.7857L23.5 9.03174L3.92857 28.373Z"
            fill="#82C68F"
          ></path>
        </svg>
      </template>
      <template v-slot:title> Track de Inglés </template>
      <template v-slot:detail>
        Sumérget en el idioma de la tecnología en sesiones diarias de
        conversacion enfocadas en el mundo profesional con otros ingenieros
        alrededor de Latinoamérica.
      </template>
    </Card>
  </div>
</template>

<script>
export default {};
</script>

<style lang="sass" scoped>
*
  transition: ease 0.5s all
.container_cards
  margin-top: 4em
  display: flex
  width: 100%
  justify-content: space-around
  align-items: center
  overflow-y: auto
  padding-left: 10px
  height: 500px
</style>
