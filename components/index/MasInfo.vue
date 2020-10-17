<template>
  <div class="masinfo">
    <div class="izq">
      <p>En Talently, te acompañamos asi:</p>
      <div class="item">
        <div class="item_icon">
          <svg
            width="40"
            height="35"
            viewBox="0 0 45 35"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <circle
              opacity="0.4"
              cx="27.7011"
              cy="6.59556"
              r="6.59556"
              fill="#FA163F"
            ></circle>
            <circle
              cx="9.23417"
              cy="6.59556"
              r="6.59556"
              fill="#FA163F"
            ></circle>
            <g opacity="0.4">
              <path
                d="M15.8303 26.3822C15.8303 20.5539 20.555 15.8293 26.3832 15.8293C32.2114 15.8293 36.9361 20.5539 36.9361 26.3822V34.2968H15.8303V26.3822Z"
                fill="#FA163F"
              ></path>
            </g>
            <g opacity="0.55">
              <path
                d="M0 26.3822C0 20.5539 4.72469 15.8293 10.5529 15.8293C16.3811 15.8293 21.1058 20.5539 21.1058 26.3822V34.2968H0V26.3822Z"
                fill="#FA163F"
              ></path>
            </g>
            <path
              d="M26.3821 22.4248L30.3395 26.3822L38.2541 18.4675"
              stroke="#FA163F"
              stroke-width="4.11968"
            ></path>
          </svg>
        </div>
        <div class="item_detail">
          <h5>Únete a sesiones de preparación intensiva</h5>
          <p>
            En temas de carrera, fundamentos de computer science e inglés, que
            potenciarán tu nivel de empleabilidad.
          </p>
        </div>
      </div>
      <div class="item">
        <div class="item_icon">
          <svg
            width="40"
            height="42"
            viewBox="0 0 58 56"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              d="M28.5907 11.224L35.3251 0L44.3042 9.42814L28.5907 11.224Z"
              fill="#AB73E1"
            ></path>
            <path
              d="M37.1209 44.8995L43.4099 51.1886L55.988 38.6105"
              stroke="#AB73E1"
              stroke-width="5.45049"
            ></path>
            <circle
              cx="11.9792"
              cy="17.9584"
              r="8.97918"
              stroke="#AB73E1"
              stroke-width="5.45049"
            ></circle>
            <rect
              x="11.9792"
              y="16.1625"
              width="34.1209"
              height="24.2438"
              fill="#AB73E1"
              style="mix-blend-mode: multiply"
            ></rect>
            <path
              d="M4.79584 49.3855C15.1219 47.7393 39.8147 36.8146 36.6719 10.326"
              stroke="#AB73E1"
              stroke-width="5.38751"
              style="mix-blend-mode: multiply"
            ></path>
          </svg>
        </div>
        <div class="item_detail">
          <h5>Recibe mentoria 1-1 con expertos</h5>
          <p>
            Te ayudarán a navegar exitosamente tus proceso de selecion y
            conseguir mejores ofertas, más rapido.
          </p>
        </div>
      </div>
      <div class="item">
        <div class="item_icon">
          <svg
            width="34"
            height="41"
            viewBox="0 0 34 41"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
            data-v-be7fd6c8=""
          >
            <rect width="4" height="41" fill="#F6C55B"></rect>
            <rect x="4" y="6" width="17" height="18" fill="#F6C55B"></rect>
            <path d="M13 24H21L13 30V24Z" fill="#F6C55B"></path>
            <g style="mix-blend-mode: multiply">
              <path
                fill-rule="evenodd"
                clip-rule="evenodd"
                d="M34 12H13V30H34L28 21L34 12Z"
                fill="#F6C55B"
              ></path>
            </g>
          </svg>
        </div>
        <div class="item_detail">
          <h5>Conecta con empresas contratando activamente</h5>
          <p>Alrededor del mundo y agiliza tu proceso de ser contratado.</p>
        </div>
      </div>
    </div>
    <div class="der">
      <ImagenDer width="100%" height="auto"></ImagenDer>
    </div>
  </div>
</template>

<script>
import ImagenDer from "~/assets/svg/index/masinfo.svg?inline";
export default {
  components: {
    ImagenDer,
  },
};
</script>

<style lang="sass" scoped>
.masinfo
  font-size: 10px
  padding: 0 1.6em
  margin-top: 2em
  color: $primary
  .der
    margin-top: 2em

  .izq
    p
      font-size: 1.6em
.item
  display: flex
  flex-direction: row
  margin-top: 2em
  &_icon
  &_detail
    padding-left: 5%
    h5
      font-size: 2em
      margin-bottom: 1em
    p
      font-size: 1.6em
@media only screen and (min-width: 768px)
  .masinfo
    padding: 0 10%

@media only screen and (min-width: 1059px)
  .masinfo
    padding: 0
    display: flex
    flex-direction: row
    justify-content: space-between
    .izq ,.der
      width: 50%
      margin-top: 0

    .izq
      padding: 0 5%
</style>
