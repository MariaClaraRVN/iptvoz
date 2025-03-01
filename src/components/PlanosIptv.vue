<template>
  <section class="planos-iptv" id="planos">
    <div class="intro">
      <h2>Escolha o plano ideal para você!</h2>
      <p class="texto-intro">
        Aproveite o melhor do IPTV com pacotes flexíveis e conteúdos exclusivos. Assista quando e onde quiser, sem
        limites!
      </p>
    </div>

    <div class="plano-popular-badge">Popular</div>

    <div class="planos-container">
      <div class="plano plano-popular">
        <h3 class="plano-titulo">Mensal</h3>
        <p class="plano-preco">R$: 30,00</p>
        <ul class="plano-beneficios">
          <li><i class="icon fa fa-check-circle" aria-hidden="true"></i>Acesso a mais de 5.000 canais</li>
          <li><i class="icon fa fa-check-circle" aria-hidden="true"></i>Qualidade HD e Full HD</li>
          <li><i class="icon fa fa-check-circle" aria-hidden="true"></i>Suporte 12h</li>
        </ul>
        <BotaoIptv />
      </div>

      <div class="plano ">
        <h3 class="plano-titulo">Trimestral</h3>
        <p class="plano-preco">R$: 80,00</p>
        <ul class="plano-beneficios">
          <li><i class="icon fa fa-check-circle" aria-hidden="true"></i>Acesso a mais de 5.000 canais</li>
          <li><i class="icon fa fa-check-circle" aria-hidden="true"></i>Qualidade HD e Full HD</li>
          <li><i class="icon fa fa-check-circle" aria-hidden="true"></i>Suporte 12h</li>
        </ul>
        <BotaoIptv />
      </div>

      <div class="plano">
        <h3 class="plano-titulo">Semestral</h3>
        <p class="plano-preco">R$: 160,00</p>
        <ul class="plano-beneficios">
          <li><i class="icon fa fa-check-circle" aria-hidden="true"></i>Acesso a mais de 5.000 canais</li>
          <li><i class="icon fa fa-check-circle" aria-hidden="true"></i>Qualidade HD e Full HD</li>
          <li><i class="icon fa fa-check-circle" aria-hidden="true"></i>Suporte 12h</li>
        </ul>
        <BotaoIptv />
      </div>

    </div>
  </section>
</template>


<script>
import BotaoIptv from './BotaoIptv.vue';

export default {
    name: 'PlanosIptv',
    components: {
        BotaoIptv
    }
}
</script>


<style scoped>
.planos-iptv {
  display: flex;
  flex-direction: column;
  padding: 20px;
/*   background-color: var(--cor-fundo-secundaria); */
  background-image: url(../assets/img/BannerNovo2.jpg); 
  backdrop-filter: blur(6px);
  background-size: cover; 
  background-position:center center;
  background-repeat: no-repeat;
  min-height: 80vh;
  color:#fff ;
}

.intro {
  padding: 5%;
  text-align: center;
  margin-bottom: 30px;
}

h2{
    font-family: var(--fonte-h1);
    color: #fff;
    font-size: 2.3rem;
    margin-bottom: 1%;
}

.texto-intro{
    color:#fff ;
    font-family: var(--fonte-texto);
    font-size: 1.5rem;
}

.planos-container {
  display: flex;
  justify-content: center;
  gap:5% ;
}

.plano {
  width: 25rem;
  background-color: var(--cor-fundo);
  padding: 20px; 
  border-radius: 8px;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
  text-align: center;
}

.plano-titulo {
  font-size: 1.5em;
  margin-bottom: 10px;
  text-align: left;
  font-family: var(--fonte-h1);
}

.plano-preco {
  font-size: 1.2em;
  font-weight: bold;
  margin-bottom: 15px;
  text-align: left;
  font-family: var(--fonte-texto);
}

.plano-beneficios {
  padding: 0;
  margin-bottom: 15px;
}

.plano-beneficios li {
  margin-bottom: 5px;
  margin-left: 1.5%;
  text-align: left;
  font-size: 1.5rem;
  font-family: var(--fonte-texto);
}

.plano-beneficios li .icon{
    color: var(--cor-icons-1);
    margin-right: 1%;
    font-size: 1rem;
}


.plano-popular-badge {
  display: flex;
  justify-content: center;
  max-width: 10%;
  background-color: #e74c3c;
  color: #fff;
  padding: 5px 10px;
  border-radius: 20px;
  font-weight: bold;
  text-align: center;
  z-index: 100;
  margin-bottom: -15px;
  margin-left: 19%;
  font-family: var(--fonte-h1);
}

@media (max-width: 768px) {
  .planos-container {
    flex-direction: column;
    align-items: center;
    gap: 20px;
  }

  .plano {
    width: 80%;
  }

  .plano-popular-badge {
    margin-left: 35%;
    max-width: 30%;
  }
}

@media (max-width: 480px) {
  h2 {
    font-size: 1.8rem;
  }

  .texto-intro {
    font-size: 1.2rem;
  }

  .plano-titulo {
    font-size: 1.2em;
  }

  .plano-preco {
    font-size: 1em;
  }

  .plano-beneficios li {
    font-size: 1.2rem;
  }

  .plano-popular-badge {
    font-size: 0.8rem;
  }
}
</style>