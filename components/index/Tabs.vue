<template>
  <div>
    <div class="tab_header">
      <button
        class="tab_links"
        @click="openCity($event,'London')"
        id="tabDefault"
      >
        <img
          src="~/assets/svg/index/proceso-admision.svg"
          alt=""
        >
        <div>
          <p> Proceso de</p>
          <span>Admisión</span>
        </div>
      </button>
      <button
        class="tab_links"
        @click="openCity($event,'Paris')"
      >
        <img
          src="~/assets/svg/index/proceso-preparacion.svg"
          alt=""
        >
        <div>
          <p> Etapa de
          </p>
          <span>Preparacion</span>
        </div>
      </button>
      <button
        class="tab_links"
        @click="openCity($event,'Tokyo')"
      >
        <img
          src="~/assets/svg/index/proceso-trabajo.svg"
          alt=""
        >
        <div>
          <p> Busqueda de</p>
          <span>Empleo</span>
        </div>
      </button>
    </div>

    <!-- Tab content -->
    <div
      id="London"
      class="tab_content"
    >
      <SeccionPreparacionItem></SeccionPreparacionItem>
      <SeccionPreparacionItem></SeccionPreparacionItem>
      <SeccionPreparacionItem></SeccionPreparacionItem>
    </div>

    <div
      id="Paris"
      class="tab_content"
    >
      <SeccionPreparacionItem></SeccionPreparacionItem>
      <SeccionPreparacionItem></SeccionPreparacionItem>
      <SeccionPreparacionItem></SeccionPreparacionItem>
    </div>

    <div
      id="Tokyo"
      class="tab_content"
    >
      <SeccionPreparacionItem></SeccionPreparacionItem>
      <SeccionPreparacionItem></SeccionPreparacionItem>
      <SeccionPreparacionItem></SeccionPreparacionItem>
    </div>
  </div>
</template>

<script>
export default {
  mounted () {
    if (process.client) {
      document.getElementById('tabDefault').click()

    }
  },
  methods: {
    openCity (evt, cityName) {
      if (process.client) {
        // Declare all variables
        var i, tab_content, tab_links;

        // Get all elements with class="tab_content" and hide them
        tab_content = document.getElementsByClassName("tab_content");
        for (i = 0; i < tab_content.length; i++) {
          tab_content[i].style.display = "none";
        }

        // Get all elements with class="tab_links" and remove the class "active"
        tab_links = document.getElementsByClassName("tab_links");
        for (i = 0; i < tab_links.length; i++) {
          tab_links[i].className = tab_links[i].className.replace(" active", "");
        }

        // Show the current tab_header, and add an "active" class to the button that opened the tab_header
        document.getElementById(cityName).style.display = "block";
        evt.currentTarget.className += " active";
      }
    }
  }
}
</script>

<style  scoped lang="scss">
.tab_header {
  overflow: hidden;
  /* Style the buttons that are used to open the tab_header content */
  button {
    color: #080863;
    border: none;
    outline: none;
    cursor: pointer;
    padding: 14px 16px;
    transition: 0.3s;
    padding: 15px 20px;
    margin-right: 12px;
    -webkit-filter: grayscale(1);
    filter: grayscale(1);
    position: relative;
    background-color: #f9f9f9;
    border-top: 3px solid transparent;
    box-shadow: inset 0 -2px 3px rgba(37, 40, 43, 0.05);
    text-decoration: none;
    align-items: center;
    white-space: nowrap;
    display: inline-flex;
    //letras
    img {
      width: 30%;
    }
    div {
      margin-left: 5%;
      p {
        font-size: 13px;
      }
      span {
        font-size: 17.6px;
      }
    }
  }
  /* Change background color of buttons on hover */
  button:hover {
  }
  /* Create an active/current tablink class */
  button.active {
    filter: grayscale(0);
    box-shadow: 0 0 8px rgba(37, 40, 43, 0.12);
    background-color: #fff;
    border-top: 2px solid #12cad6;
  }
}

/* Style the tab_header content */
.tab_content {
  background-color: #fff;
  box-shadow: 0 0 8px rgba(37, 40, 43, 0.12);
  display: flex;
  overflow: hidden;
  border-bottom-left-radius: 8px;
  border-bottom-right-radius: 8px;
}

//EFECTOS
.tab_content {
  animation: fadeEffect 1s; /* Fading effect takes 1 second */
}

/* Go from zero to full opacity */
@keyframes fadeEffect {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
</style>
