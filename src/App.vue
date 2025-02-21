<template>
  <HeaderIptv/>
  <HomeIptv/>
  <EscolhaIptv/>
  <PlanosIptv/>
  <MissaoIptv/>
  <SuporteIptv/>
  <FormIptv/>
  <FooterIptv/>

</template>

<script>
import EscolhaIptv from './components/EscolhaIptv.vue';
import FormIptv from './components/FormIptv.vue';
import HeaderIptv from './components/HeaderIptv.vue';
import HomeIptv from './components/HomeIptv.vue';
import MissaoIptv from './components/MissaoIptv.vue';
import PlanosIptv from './components/PlanosIptv.vue';
import SuporteIptv from './components/SuporteIptv.vue';
import FooterIptv from './components/FooterIptv.vue';

export default {
  name: 'App',
  components: {
    HeaderIptv,
    HomeIptv,
    EscolhaIptv,
    PlanosIptv,
    MissaoIptv,
    FormIptv,
    SuporteIptv,
    FooterIptv
  }
}
</script>

<style>
* { 
   margin: 0;
   padding: 0;
   box-sizing:border-box;
   list-style: none;
   text-decoration: none;
   overflow-x: hidden;
   scroll-behavior: smooth;
} 

/* Cores */
:root {
  --cor-primaria: #FFCC00;
  --cor-secundaria: #FF9900;
  --cor-icons-1: #00FF88;
  --cor-icons-2:#007b5e;
  --cor-icons-3:#ce1414; 
  --cor-fundo: #0A2239;
  --cor-fundo-secundaria: #061624;
  --cor-texto: white;
  --fonte-texto:"Montserrat";
  --fonte-titulo: "Rowdies" , serif;
  --fonte-h1: "Kanit", serif
}


</style>
