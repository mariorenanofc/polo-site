<template>
  <div>
    <img alt="Vue logo" src="./assets/logo.png" id="logo-home" />
    <Login msg="Bem-vindo ao Polo da Sorte" />
    <!--<InicioSorte />-->
  </div>
</template>

<script>
import Login from './components/Login.vue'

export default {
  name: 'App',
  components: {
    Login,
  },
  mounted() {
    const logo = document.getElementById('logo-home');
    setTimeout(() => {
      this.rotateLogo(logo);
    }, 500); // Aguarda 1 segundo (ajuste conforme necessário)
  },
  methods: {
  rotateLogo(logo) {
    let rotation = 0;
    const interval = setInterval(() => {
      rotation += 18; // Ajuste o ângulo da rotação conforme necessário
      logo.style.transform = `rotateY(${rotation}deg)`;
      if (rotation >= 360) {
        clearInterval(interval);
        setTimeout(() => {
          logo.style.transform = 'rotateY(0deg)';
        }, 500); // Tempo de espera para retornar à posição original (ajuste conforme necessário)
      }
    }, 25); // Ajuste o intervalo de tempo entre cada rotação conforme necessário

    setTimeout(() => {
      clearInterval(interval);
      logo.style.transform = 'rotateY(0deg)';
    }, 10000); // Tempo total de rotação em milissegundos (10 segundos)
  }
}



}
</script>


<style>
* {
  padding: 0;
  margin: 0;
  box-decoration-break: 0;
}
body {
  padding: 0;
  margin: 0;
  box-decoration-break: 0;
}

@font-face {
  font-family: "Montserrat Italic";
  src: url("@/assets/fonts/Montserrat-Italic-VariableFont_wght.ttf");
}

@font-face {
  font-family: "Lexend Deca";
  src: url(@/assets/fonts/LexendDeca-VariableFont_wght.ttf);
}

#app {
  font-family: "Montserrat Italic";
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

body {
  background-color: #DAE2DF;
}

#logo-home {
  width: 15vw;
  height: 15vw;
  max-width: 200px; /* Define um tamanho máximo para evitar que a imagem fique muito grande em telas maiores */
  max-height: 200px;
  margin-bottom: 2rem;
  margin-top: 2rem;
  transition: transform 0.5s ease;
}

</style>
