<template>
  <section class="secao-inicio" id="inicio">
    <div class="secao-conteudo">
      <article class="conteudo">
        <h1>TV COM TUDO LIBERADO + SÉRIES E FILMES!</h1>
        <p>Tenha acesso a todos os seus streamings favoritos em um só lugar por um preço acessível. Canais ao vivo,
          filmes, séries e muito mais, com qualidade HD e suporte garantido.</p>

        <h3>Compatível com todos os dispositivos!</h3>
        <p>Assista quando e onde quiser, na sua Smart TV, TV Box, celular ou computador.</p>
        <BotaoIptv />
      </article>

      <div class="imagem">
        <img src="../assets/img/streaming.png" alt="">
      </div>
    </div>
  </section>
</template>
  

<script>
import BotaoIptv from './BotaoIptv.vue';


export default{
    name: 'HomeIptv',
    components:{
        BotaoIptv,
        
    }
}
</script>

<style scoped>
.secao-inicio {
  width: 100vw;
  background-image: url('../assets/img/BannerNovo.jpg');
  backdrop-filter: blur(6px);
  background-size: cover; 
  background-position:center center;
  background-repeat: no-repeat;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center; 
  align-items: flex-start; 
  text-align: left;
  color: white;
  padding: 20px 10%;
  outline: none;
}
.secao-conteudo{
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 100%;

}

.conteudo {
  border-radius: 18px;
  max-width: 45%; 
  margin-top: 10%; 
  margin-bottom: 2%;
}

h1{
  font-family: var(--fonte-h1);
  font-size: 2rem;
}


h3{
  font-family: var(--fonte-h1);
  font-size: 1.5rem;
}

p{
  font-family: var(--fonte-texto);
  font-size: 1.3rem;
  margin-bottom: 5%
}

.imagem img{
  max-width: 80%;
  align-items: center;
  margin-top: 10%;
  margin-left: 10%;
}

@media (max-width: 768px) {
  .secao-inicio {
    padding: 20px 5%;
    align-items: center;
    text-align: center;
  }

  .conteudo {
    max-width: 80%;
    margin-top: 20%;
  }

  h1 {
    font-size: 1.8rem;
  }

  p {
    font-size: 1.1rem;
  }
}

@media (max-width: 768px) {
  .secao-inicio {
    padding: 20px 5%;
    align-items: center;
    text-align: center;
  }

  .secao-conteudo {
    flex-direction: column;
  }

  .conteudo {
    max-width: 80%;
    margin-top: 20%;
  }

  h1 {
    font-size: 1.8rem;
  }

  p {
    font-size: 1.1rem;
  }

  .imagem img {
    max-width: 100%;
    margin-top: 20px;
    margin-left: 0;
  }
}

@media (max-width: 480px) {
  .secao-inicio {
    padding: 20px 2%;
  }

  .conteudo {
    max-width: 90%;
    margin-top: 30%;
  }

  h1 {
    font-size: 1.5rem;
  }

  p {
    font-size: 1rem;
  }

  .imagem img {
    max-width: 100%;
    margin-top: 20px;
    margin-left: 0;
  }
}
</style>