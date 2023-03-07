<template>
  <div class="home">
    <header class="header">
      <nav class="navbar">
        <div class="logo">
          <img src="@/assets/logo.png" alt="Polo da Sorte Logo" />
        </div>
        <ul class="nav-links">
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
            <img src="#" alt="Jogo 1" />
            <h3 class="game-title">Mega Sorteio</h3>
            <p class="game-desc">
              Aposte nos seus números da sorte e concorra a prêmios milionários
              em dinheiro.
            </p>
            <button class="btn-game">Jogar agora</button>
          </div>
          <div class="game-card">
            <img src="#" alt="Jogo 2" />
            <h3 class="game-title">Bingo da Sorte</h3>
            <p class="game-desc">
              Marque seus números no cartão de bingo e concorra a prêmios em
              dinheiro e outros prêmios incríveis.
            </p>
            <button class="btn-game">Jogar agora</button>
          </div>
          <div class="game-card">
            <img src="#" alt="Jogo 3" />
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
};
</script>

<style scoped>
  .home {
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
    height: 90px;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    align-items: center;
    padding: 0 5%;
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
    border: none;
    border-radius: 5px;
    padding: 10px;
    color: #fff;
    background-color: #42b983;
    font-weight: bold;
    cursor: pointer;
    transition: background-color 0.3s ease;
    box-shadow: 0 2px 5px rgba(0, 0, 0, 0.3);
  }

  .account button:hover {
    background-color: #239267;
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
  padding: 50px 0;
  font-size: 16px;
  color: #6d6d6d;
}

.footer-container {
  max-width: 1200px;
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