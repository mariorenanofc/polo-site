<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h2>Sorteios todo mês</h2>
    <form class="login-form" action="">
      <h3>{{ subTitulo }}</h3>
        <div class="container-titulo">
          <p>Login</p>
        </div>
      <div class="input-group">
        <input
          type="text"
          id="username"
          v-model="username"
          placeholder="Digite seu usuário"
        />
      </div>
      <div class="input-group">
        <input
          type="password"
          id="password"
          v-model="password"
          placeholder="Digite sua senha"
        />
      </div>
      <p class="error-message" v-if="showErrorMessage">{{ errorMessage }}</p>
      <button class="login-button" v-on:click="entrar">
        <span v-if="loading">⏳ Carregando...</span>
        <span v-else>Entrar</span>
      </button>
      <p class="forgot-password">{{ EsqueceuSenha }} Esqueceu a Senha</p>
      <p class="create-user">{{ createUser }} Cadastre-se Aqui!</p>
    </form>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  subTitulo: "Login",
  props: {
    msg: String,
  },
  data() {
    return {
      username: "",
      password: "",
      showErrorMessage: false,
      errorMessage: "Usuário ou senha incorretos, tente novamente!",
      loading: false
    };
  },
  methods: {
    entrar() {
      this.loading = true;

      if (this.username === "admin" && this.password === "admin") {
        setTimeout(() => {
          alert("Login realizado com sucesso!");
          this.loading = false;
        }, 3000);
      } else {
        setTimeout(() => {
          this.showErrorMessage = true;
          this.loading = false;
          setTimeout(() => {
            this.showErrorMessage = false;
          }, 10000);
        }, 3000);
      }
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

.container-titulo{
  font-family: 'Montserrat Italic';
  color: #1E6A2D;
  font-size: 4vh;
  text-transform: uppercase;
  font-weight: bolder;
  letter-spacing: 2px;
}
.hello {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 100%;
  width: 100%;
  margin-top: 10px;
  
}

.hello h1 {
  margin-top: 10px;
}
.hello h2 {
  margin:28px 0 40px 0;
}

.login-form {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  font-family: "Lexend Deca";
  padding: 20px;
  border: 1px solid #ccc;
  border-radius: 5px;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.3);
  width: 80%;
  max-width: 400px;
  background-color: #42b9835f;
}

.input-group {
  display: flex;
  flex-direction: row;
  align-items: center;
  margin-bottom: 20px;
}

.input-group label {
  font-weight: bold;
  margin-right: 10px;
}

.input-group input {
  padding: 10px 35px;
  border: 1px solid #ccc;
  border-radius: 10px;
  width: 100%;
  max-width: 250px;
  background-color: #58956E;
  color: #F9EA76;
  text-align: center;
}

.input-group input::placeholder{
  color: #FCCB06;
  text-align: center;
  
}

.input-group input:focus{
  border: 2px solid #42b983;
  background: #F9EA76;
  outline: none;
  color: #239267;
}


.error-message {
  display: block;
  margin-top: 8px;
  padding: 4px;
  color: #dc3545;
  font-weight: 700;
  border-radius: 4px;
}

.login-button {
  padding: 10px 50px;
  background-color: #42b983;
  border: none;
  border-radius: 5px;
  color: #fff;
  font-weight: bold;
  cursor: pointer;
  transition: background-color 0.2s ease;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.3);
  margin: 15px 0;
}

.login-form .forgot-password,
.login-form .create-user {
  color: #1E6A2D;
  margin: 16px 0 0 0;
}

.login-button:hover {
  background-color: #FCCB06;
  color: #1E6A2D;
  border-radius: 8px;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.3);
}

.login-links {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  margin-top: 20px;
  width: 100%;
}

.login-links p {
  margin: 0;
  color: #42b983;
  font-weight: bold;
  cursor: pointer;
}

/* Estilos para dispositivos com largura mínima de 280px */
@media screen and (max-width: 280px) {
  .hello {
    font-size: 10px;
  }
  .hello h1, h2 {
    display: none;
  }

  .container-titulo {
    font-size: 24px;
    letter-spacing: 1px;
  }
  .input-group input {
    padding: 8px 30px;
    max-width: 200px;
    font-size: 14px;
  }
  .login-button {
    padding: 8px 40px;
    font-size: 16px;
  }
  .forgot-password,
  .create-user {
    font-size: 12px;
  }
}

/* Estilos para dispositivos com largura mínima de 450px */
@media screen and (max-width: 450px ) {
  .hello {
    font-size: 12px;
  }
  .hello h1, h2 {
    display: none;
  }
  .container-titulo {
    font-size: 28px;
    letter-spacing: 2px;
  }
  .input-group input {
    padding: 10px 35px;
    max-width: 250px;
    font-size: 16px;
  }
  .login-button {
    padding: 10px 50px;
    font-size: 18px;
  }
  .forgot-password,
  .create-user {
    font-size: 14px;
  }
}

</style>
