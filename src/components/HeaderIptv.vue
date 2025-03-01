<template>
  <header class="cabecalho">
    <nav class="navegacao">
      <div class="logo">
        <i class="fa fa-television" aria-hidden="true"></i>
        <a href="#">IPTVOz</a>
      </div>

      <div class="menu-toggle" @click="toggleMenu">
        <i class="fa icone-menu" :class="menuOpen ? 'fa-times' : 'fa-bars'" aria-hidden="true"></i>
      </div>

      <ul class="menu" :class="{ 'menu-open': menuOpen }">
        <li><a href="#inicio">Início</a></li>
        <li><a href="#planos">Planos</a></li>
        <li><a href="#sobre">Sobre</a></li>
        <li><a href="#suporte">Suporte</a></li>
        <li><a href="#contato">Contato</a></li>
      </ul>
      <BotaoIptv v-if="!menuOpen" class="botao-teste" />
    </nav>
  </header>
</template>

<script>
import BotaoIptv from './BotaoIptv.vue';

export default {
  name: 'HeaderIptv',
  components: {
    BotaoIptv
  },
  data() {
    return {
      menuOpen: false
    };
  },
  methods: {
    toggleMenu() {
      this.menuOpen = !this.menuOpen;
    }
  }
}
</script>

<style scoped>
.cabecalho {
  background: var(--cor-fundo);
  backdrop-filter: blur(16px);
  width: 100%;
  position: fixed;
  z-index: 50;
  padding: 16px 0;
}

.navegacao {
  display: flex;
  justify-content: space-between;
  align-items: center;
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 16px;
}

.logo {
  display: flex;
  align-items: center;
  gap: 8px;
  font-family: var(--fonte-titulo);
  line-height: normal;
}

.logo i {
  font-size: 1.5rem;
  color: var(--cor-primaria);
  line-height: normal;
}

.logo i:hover {
  color: var(--cor-secundaria);
}

.logo a {
  font-size: 1.5rem;
  font-weight: bold;
  color: var(--cor-texto);
  text-decoration: none;
}

.menu {
  display: flex;
  gap: 24px;
  font-family: var(--fonte-texto);
}

.menu li {
  list-style: none;
  border-bottom: 2px solid transparent;
  transition: border-color 0.3s ease-in-out;
}

.menu li:hover {
  border-bottom: 2px solid var(--cor-primaria);
}

.menu a {
  color: var(--cor-texto);
  text-decoration: none;
  font-size: 1.3rem;
  transition: color 0.3s;
}

.menu a:hover {
  color: var(--cor-primaria);
}

.botao-teste {
  background-color: var(--cor-primaria);
  color: var(--cor-fundo);
  padding: 8px 16px;
  border-radius: 999px;
  font-weight: 600;
  text-decoration: none;
  transition: background-color 0.3s;
  font-family: var(--fonte-texto);
  display: flex;
  justify-content: center;
  text-align: center;
  margin-top: 16px;
}

.botao-teste:hover {
  background-color: var(--cor-secundaria);
}

.menu-toggle {
  display: none;
  font-size: 1.5rem;
  color: var(--cor-texto);
  cursor: pointer;
}

@media (max-width: 768px) {
  .navegacao {
    flex-wrap: wrap;
    justify-content: space-between;
  }

  .menu {
    flex-direction: column;
    gap: 16px;
    width: 100%;
    align-items: flex-start;
    margin-top: 16px;
    display: none;
  }

  .menu.menu-open {
    display: flex;
  }

  .icone-menu {
    line-height: normal;
  }

  .menu-toggle {
    display: block;
  }

  .botao-teste {
    justify-content: center;
    width: 100%;
    text-align: center;
    margin: 5% 0 0 5%;
  }
}

@media (max-width: 480px) {
  .logo i, .logo a {
    font-size: 1.2rem;
  }

  .menu a {
    font-size: 1rem;
  }

  .botao-teste {
    font-size: 1rem;
    padding: 8px 12px;
  }
}
</style>