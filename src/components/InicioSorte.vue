<template>
  <div class="home">
    <header class="header">
      <nav class="navbar">
  <div class="logo">
    <img src="@/assets/menu-mobile.svg" alt="Polo da Sorte Logo" />
  </div>
  <img src="caminho/para/imagem.svg" alt="Menu" class="menu-icon" @click="toggleMenu">
  <ul class="nav-links" v-show="showMenu">
    <li><a href="#">Jogos</a></li>
    <li><a href="#">Resultados</a></li>
    <li><a href="#">Como Jogar</a></li>
    <li><a href="#">Sobre Nós</a></li>
  </ul>
  <div class="account">
    <button class="btn-login">Entrar</button>
    <button class="btn-signup">Cadastrar</button>
  </div>
</nav>
      <div class="hero">
        <h1 class="title">Bem-vindo ao Polo da Sorte</h1>
        <p class="subtitle">Jogue, divirta-se e ganhe prêmios incríveis</p>
        <button class="btn-cta">Jogue agora</button>
      </div>
    </header>
    <section class="about">
      <div class="container">
        <h2 class="section-title">Sobre Nós</h2>
        <p class="section-desc">
          O Polo da Sorte é um site de apostas online onde você pode jogar em
          diversos jogos e concorrer a prêmios incríveis. Nós estamos em
          constante evolução e sempre trazendo novas opções de jogos e prêmios
          para nossos jogadores.
        </p>
      </div>
    </section>
    <section class="games">
      <div class="container">
        <h2 class="section-title">Jogos</h2>
        <div class="game-cards">
          <div class="game-card">
            <img src="@/assets/mega-sorteio.jpg" alt="Jogo 1" />
            <h3 class="game-title">Mega Sorteio</h3>
            <p class="game-desc">
              Aposte nos seus números da sorte e concorra a prêmios milionários
              em dinheiro.
            </p>
            <button class="btn-game">Jogar agora</button>
          </div>
          <div class="game-card">
            <img src="@/assets/bingo-sorte.jpg" alt="Jogo 2" />
            <h3 class="game-title">Bingo da Sorte</h3>
            <p class="game-desc">
              Marque seus números no cartão de bingo e concorra a prêmios em
              dinheiro e outros prêmios incríveis.
            </p>
            <button class="btn-game">Jogar agora</button>
          </div>
          <div class="game-card">
            <img src="@/assets/roleta-sorte.jpg" alt="Jogo 3" />
            <h3 class="game-title">Roleta da Sorte</h3>
            <p class="game-desc">
              Faça sua aposta na roleta e torça para a sorte estar ao seu lado
              nesse emocionante jogo de cassino.
            </p>
            <button class="btn-game">Jogar agora</button>
          </div>
        </div>
      </div>
    </section>
    <footer class="footer">
      <div class="footer-container">
        <div class="footer-column">
          <h3 class="footer-title">Contato</h3>
          <ul class="footer-list">
            <li class="footer-list-item">
              <a href="tel:+5511999999999">11 99999-9999</a>
            </li>
            <li class="footer-list-item">
              <a href="mailto:contato@polodasorte.com.br"
                >contato@polodasorte.com.br</a
              >
            </li>
            <li class="footer-list-item">
              <a href="#">Formulário de contato</a>
            </li>
          </ul>
        </div>

        <div class="footer-column">
          <h3 class="footer-title">Sobre</h3>
          <ul class="footer-list">
            <li class="footer-list-item">
              <a href="#">Sobre a Polo da Sorte</a>
            </li>
            <li class="footer-list-item"><a href="#">Termos de uso</a></li>
            <li class="footer-list-item">
              <a href="#">Política de privacidade</a>
            </li>
          </ul>
        </div>

        <div class="footer-column">
          <h3 class="footer-title">Redes sociais</h3>
          <ul class="footer-list">
            <li class="footer-list-item"><a href="#">Facebook</a></li>
            <li class="footer-list-item"><a href="#">Twitter</a></li>
            <li class="footer-list-item"><a href="#">Instagram</a></li>
          </ul>
        </div>
      </div>

      <div class="footer-bottom">
        <p class="footer-copy">
          © 2023 Polo da Sorte. Todos os direitos reservados.
        </p>
      </div>
    </footer>
  </div>
</template>
<script>
export default {
  name: "InicioSorte",
  data() {
    return {
      showMenu: false
    }
  },
  methods: {
    toggleMenu() {
      this.showMenu = !this.showMenu
    }
  }
}
</script>

<style scoped>
.home {
  max-width: 100%;
  font-family: "Lexend Deca";
  background-color: #fff;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding-top: 30px;
}

.header {
  width: 100%;
  margin-bottom: 100px;
  height: 90px;
  display: flex;
  flex-wrap: nowrap;
  justify-content: space-around;
  padding: 0 5%;
  flex-direction: column;
}

.navbar {
  position: initial;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  width: 100%;
  background: #239267;
}

.logo img {
  height: 40px;
  margin: 17px;
}

.hamburger-menu {
  display: none;
  cursor: pointer;
}

.bar {
  width: 25px;
  height: 3px;
  background-color: #fff;
  margin: 5px 0;
}

@media screen and (max-width: 840px) {
  .nav-links {
    display: none;
  }
  .navbar {
    flex-direction: column;
    align-items: flex-start;
    padding: 10px;
  }
  .nav-links li {
    text-align: center;
    width: 100%;
    margin: 10px 0;
  }
  .nav-links li a {
    font-size: 16px;
    padding: 10px;
    border-radius: 5px;
  }
  .hamburger-menu {
    display: flex;
  }
  .account {
    margin-top: 10px;
  }
}

.nav-links {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  width: 50%;
  list-style-type: none;
}

.nav-links li a {
  font-weight: bold;
  text-decoration: none;
  color: #2c3e50;
  transition: color 0.3s ease;
  padding: 10px;
  border-radius: 5px;
}

.nav-links li a:hover {
  color: #42b983;
  background-color: #f2f2f2;
}

.account button {
  display: flex;
  width: 74px;
  height: 30px;
  border: none;
  border-radius: 5px;
  margin: 4px 8px;
  font-weight: bold;
  cursor: pointer;
  transition: background-color 0.3s ease;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.3);
  justify-content: center;
}

.account button:hover {
  background-color: #fccb06;
  color: #2c3e50;
}

.account .btn-login,
.btn-signup {
  font-size: 12px;
  text-align: center;
  padding: 10px;
  color: #fff;
  background-color: #42b983;
}

@media screen and (max-width: 840px) {
  .navbar {
    flex-direction: initial;
    justify-content: center;
    align-items: center;
  }

  .logo img {
    margin: 20px 0;
  }

  .nav-links {
    flex-direction: column;
    justify-content: center;
    align-items: center;
    width: 100%;
    height: 0;
    overflow: hidden;
    transition: height 0.3s ease;
  }

  .nav-links.show {
    height: 200px;
  }

  .nav-links li {
    width: 100%;
    text-align: center;
    padding: 10px;
  }

  .nav-links li a {
    display: block;
    padding: 10px;
    border-radius: 5px;
    color: #2c3e50;
    transition: color 0.3s ease;
  }

  .nav-links li a:hover {
    color: #42b983;
    background-color: #f2f2f2;
  }

  .menu-icon {
    display: block;
    position: absolute;
    top: 0;
    right: 0;
    cursor: pointer;
    padding: 20px;
    z-index: 1;
  }

  .menu-icon .bars {
    display: block;
    width: 25px;
    height: 3px;
    background-color: #fff;
    border-radius: 5px;
    margin: 5px 0;
    transition: transform 0.3s ease-in-out;
  }

  .menu-icon .bars:nth-child(1) {
    transform: rotate(45deg) translate(5px, 5px);
  }

  .menu-icon .bars:nth-child(2) {
    opacity: 0;
  }

  .menu-icon .bars:nth-child(3) {
    transform: rotate(-45deg) translate(5px, -5px);
  }

  .menu-icon.active .bars:nth-child(1) {
    transform: rotate(0) translate(0, 0);
  }

  .menu-icon.active .bars:nth-child(2) {
    opacity: 1;
  }

  .menu-icon.active .bars:nth-child(3) {
    transform: rotate(0) translate(0, 0);
  }
}

.hero-section {
  width: 100%;
  height: 60vh;
  display: flex;
  justify-content: center;
  align-items: center;
  background-image: url("https://images.unsplash.com/photo-1525241087022-2eadeb2dab55?ixid=MXwxMjA3fDB8MHxzZWFyY2h8Nnx8cG9sb3xlbnwwfHwwfA%3D%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60");
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
}

.hero-section h1 {
  font-size: 4rem;
  color: #fff;
  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.6);
  text-align: center;
  text-transform: uppercase;
  letter-spacing: 3px;
}

.hero-section p {
  font-size: 1.5rem;
  color: #fff;
  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.6);
  text-align: center;
  margin-top: 20px;
}

.games-section {
  width: 100%;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
  padding: 50px 5%;
}

.game-card {
  width: 30%;
  margin: 20px;
  background-color: #fff;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);
  border-radius: 5px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  overflow: hidden;
  position: relative;
}

.game-card img {
  width: 100%;
  height: auto;
  object-fit: cover;
}

.game-card .game-info {
  padding: 20px;
}

.game-card .game-info h3 {
  margin-top: 0;
  margin-bottom: 10px;
  font-size: 1.5rem;
  font-weight: 500;
}

.game-card .game-info p {
  margin: 0;
  font-size: 1rem;
  color: #666;
}

.game-card .game-actions {
  padding: 10px 20px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  background-color: #f7f7f7;
}

.game-card .game-actions button {
  border: none;
  background-color: #0084ff;
  color: #fff;
  padding: 10px 20px;
  border-radius: 3px;
  font-size: 1rem;
  cursor: pointer;
}

.game-card .game-actions button:hover {
  background-color: #0056b3;
}

/* Estilos para o footer */

.footer {
  background-color: #f4f4f4;
  padding: 0;
  font-size: 16px;
  color: #6d6d6d;
  width: 100%;
}

.footer-container {
  margin: 0 auto;
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
}

.footer-column {
  flex-basis: 30%;
  margin-bottom: 30px;
}

.footer-title {
  font-size: 18px;
  margin-bottom: 15px;
}

.footer-list {
  list-style: none;
  margin: 0;
  padding: 0;
}

.footer-list-item {
  margin-bottom: 10px;
}

.footer-list-item a {
  color: #6d6d6d;
  text-decoration: none;
}

.footer-list-item a:hover {
  text-decoration: underline;
}

.footer-bottom {
  background-color: #e0e0e0;
  padding: 20px 0;
  margin-top: 30px;
}

.footer-copy {
  font-size: 14px;
  color: #6d6d6d;
  text-align: center;
  margin: 0;
}
</style>