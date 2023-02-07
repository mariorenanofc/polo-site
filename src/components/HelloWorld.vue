<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h2>Sorteios todo mês</h2>
    <form action="">
      <h3>{{ subTitulo }}</h3>
      <input type="text" v-model="username" placeholder="Usuário" >
      <input type="password" v-model="password" placeholder="Senha" >
      <button v-on:click="entrar">Entrar</button>

      <p>{{ EsqueceuSenha }}</p>
      <p>{{ NoRegister }}</p>
      <p>{{ createUser }}</p>
    </form>
    
    
    
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
    subTitulo: "Login",
  props: {
    msg: String,
  },
  data () {
      return {
        username: "",
        password: ""
      };
    },
  methods: {
    entrar() {
      if(this.username == "admin" &&  this.password  == "admin"){
        alert("Login Realizado com Sucesso!");
      }
      else {
        alert("Usuário ou senha incorretos, Tente Novamente!");
      }
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>



h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
