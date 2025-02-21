<template>
    <section class="faq">
      <h2 class="titulo">Dúvidas <span>Frequentes</span></h2>
      
      <div class="faq-container">
        <div 
          v-for="(pergunta, index) in perguntas" 
          :key="index" 
          class="faq-item"
        >
          <button class="faq-pergunta" @click="togglePergunta(index)">
            {{ pergunta.questao }}
            <span class="icone">{{ pergunta.aberta ? "▲" : "▼" }}</span>
          </button>
          <p v-if="pergunta.aberta" class="faq-resposta">{{ pergunta.resposta }}</p>
        </div>
      </div>
    </section>
  </template>
  
  <script>
  export default {
    name: 'SuporteIptv',
    data() {
      return {
        perguntas: [
          { questao: "Como posso entrar em contato?", resposta: "Você pode me enviar um e-mail ou usar o formulário de contato.", aberta: false },
          { questao: "Quais tecnologias você usa?", resposta: "Eu utilizo Vue.js, Tailwind CSS, Firebase e outras ferramentas modernas.", aberta: false },
          { questao: "Você aceita projetos freelancer?", resposta: "Sim! Entre em contato para discutirmos sua ideia.", aberta: false },
          { questao: "Você aceita projetos freelancer?", resposta: "Sim! Entre em contato para discutirmos sua ideia.", aberta: false },
          { questao: "Você trabalha com WordPress?", resposta: "Atualmente, foco em desenvolvimento com Vue.js e React, mas podemos conversar sobre soluções alternativas.", aberta: false }
        ]
      };
    },
    methods: {
      togglePergunta(index) {
        this.perguntas[index].aberta = !this.perguntas[index].aberta;
      }
    }
  };
  </script>
  
  <style scoped>
  .faq {
    padding: 40px;
    background-color: var(--cor-fundo-secundaria);
    text-align: center;
  }
  
  .titulo {
    font-size: 2em;
    margin-bottom: 20px;
    font-family: var(--fonte-titulo);
    color: #fff;
  }
  
  .titulo span {
    color: var(--cor-primaria);
  }
  
  .faq-container {
    max-width: 600px;
    margin: 0 auto;
    text-align: left;
  }
  
  .faq-item {
    border-bottom: 2px solid var(--cor-fundo);
    padding: 10px 0;
  }
  
  .faq-pergunta {
    width: 100%;
    background: none;
    border: none;
    font-size: 1.2em;
    text-align: left;
    cursor: pointer;
    display: flex;
    justify-content: space-between;
    padding: 10px;
    color: #fff;
    font-weight: bold;
    font-family: var(--fonte-texto);
  }
  
  .icone {
    color: var(--cor-icons-1);
    transition: transform 0.3s ease;
  }
  
  .faq-resposta {
    padding: 10px;
    font-size: 1em;
    color: #fff;
    font-family: var(--fonte-texto);
  }

  @media (max-width: 768px) {
  .faq {
    padding: 30px 20px;
  }

  .faq-container {
    max-width: 100%;
    padding: 0 10px;
  }

  .faq-pergunta {
    font-size: 1em;
    padding: 12px;
  }

  .faq-resposta {
    font-size: 0.95em;
    padding: 8px 12px;
  }

  .icone {
    font-size: 1em;
  }
}

  </style>
  