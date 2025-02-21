<template>
    <section class="secao-inicio">
      <article class="conteudo">
        <h1>Lorem ipsum, dolor sit amet consectetur.</h1>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Architecto vel dignissimos tempore fugiat blanditiis neque, quasi saepe incidunt aut in. Enim, minus voluptas? Aliquid non exercitationem, debitis consequatur cum numquam?</p>
      </article>
      <BotaoIptv />
    </section>
  </template>
  

<script>
import BotaoIptv from './BotaoIptv.vue';

export default{
    name: 'HomeIptv',
    components:{
        BotaoIptv
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

p{
  font-family: var(--fonte-texto);
  font-size: 1.3rem;
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
}
</style>