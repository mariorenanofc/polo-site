<template>
  <div>
    <img alt="Vue logo" src="./assets/logo.png" id="logo-home" />
    <Login msg="Bem vindo ao Polo da Sorte" />
    <InicioSorte />
  </div>
</template>

<script>
import InicioSorte from './components/InicioSorte.vue'
import Login from './components/Login.vue'


export default {
  name: 'App',
  components: {
    Login,
    InicioSorte
    
  }
}
</script>

<style>
@font-face {
    font-family: "Montserrat Italic";
    src: url("@/assets/fonts/Montserrat-Italic-VariableFont_wght.ttf");

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
  width: 15%;
  height: 15%;
}
</style>
