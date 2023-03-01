
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
      <button class="login-button" v-on:click="entrar">Entrar</button>
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
    };
  },
  methods: {
    entrar() {
      if (this.username === "admin" && this.password === "admin") {
        alert("Login realizado com sucesso!");
      } else {
        alert("Usuário ou senha incorretos, tente novamente!");
      }
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

.container-titulo{
  font-family: 'Inter';
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
}

.login-form {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
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

/* Estilos para dispositivos com largura máxima de 768px */
@media screen and (max-width: 768px) {
  .input-group {
    flex-direction: column;
    margin-bottom: 10px;
  }
  label {
    margin-bottom: 5px;
  }
}
/* Estilos para dispositivos com largura mínima de 769px */
@media screen and (min-width: 769px) {
  .input-group {
    display: flex;
    justify-content: space-between;
    margin-bottom: 20px;
  }
  label {
    width: 30%;
    margin-right: 10px;
    text-align: right;
  }
  input {
    width: 65%;
  }
}
button {
  background-color: #42b983;
  color: white;
  border: none;
  border-radius: 5px;
  padding: 10px 20px;
  margin-top: 10px;
  cursor: pointer;
}
button:hover {
  background-color: #239267;
}
.forgot-password,
.register,
.create-user {
  font-size: 12px;
  margin-top: 5px;
}
.forgot-password {
  text-align: center;
  text-decoration: underline;
}
.register,
.create-user {
  text-align: center;
}
</style>
