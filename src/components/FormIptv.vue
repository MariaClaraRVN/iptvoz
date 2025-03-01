<template>
  <section class="contato" id="contato">
    <h2 class="titulo">Contate <span>- Me</span></h2>
    <p class="descricao">
      Tem alguma dúvida ou quer saber mais? <br> Fale conosco e descubra como podemos transformar sua experiência com
      IPTV!
    </p>

    <div class="conteudo-contato">
      <div class="informacoes-contato">
        <h4 class="subtitulo">Contate - me</h4>
        <ul class="lista-contato">
          <li>Email: gustavokaph@gmail.com</li>
          <li>Telefone: (11) 91827-6555</li>
        </ul>
        <h4 class="subtitulo">Suporte</h4>
        <p class="horario">Segunda à Sabádo das 08h às 22h</p>
        <p class="horario">Domingos das 10h às 18h</p>
      </div>

      <div class="borda"></div>

      <div class="formulario">
        <form action="https://formsubmit.co/gustavokaph@gmail.com" method="POST">
          <input type="hidden" name="_captcha" value="false">
          <input type="hidden" name="_template" value="table">
          <input type="hidden" name="_subject" value="Novo contato para o IPTVOz!">
          <input type="hidden" name="_next" value="https://www.iptvoz.com.br/">

          <div class="grupo-input">
            <div class="caixa-input">
              <input type="text" name="nome" placeholder="Nome Completo" required>
              <input type="email" name="email" placeholder="Email" required>
            </div>
            <div class="caixa-input">
              <input type="tel" name="telefone" placeholder="Número de Celular">
            </div>
          </div>

          <div class="grupo-input-mensagem">
            <textarea name="mensagem" cols="30" rows="10" placeholder="Sua Mensagem" required></textarea>
            <input type="submit" value="Enviar Mensagem" class="botao">
          </div>
        </form>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'FormIptv'
}
</script>


<style scoped>
.contato {
  padding: 5% 0;
  background-color: var(--cor-fundo);
  text-align: center;
  color: #fff;
  height: 90%;
}

.titulo {
  font-size: 2em;
  margin-bottom: 20px;
  font-family: var(--fonte-h1);
}

.titulo span {
  color: var(--cor-primaria);
}

.descricao {
  font-size: 1.2em;
  margin-bottom: 20px;
  color: #fff;
  font-family: var(--fonte-texto);
  margin-bottom: 6%;
}

.conteudo-contato {
  display: flex;
  justify-content: space-between;
  width: 100%;
}

.informacoes-contato {
  max-width: 300px;
  text-align: left;
  margin-left: 16%;
}

.subtitulo {
  font-size: 1.4em;
  margin-bottom: 10px;
  font-family: var(--fonte-titulo);
  margin-bottom: 6%;
}

.lista-contato {
  list-style: none;
  padding: 0;
  margin-bottom: 15px;
}

.lista-contato li {
  padding: 5px 0;
  font-family: var(--fonte-texto);
  margin-bottom: 4%;
}

.horario {
  color:#fff;
  font-size: 1em;
  margin-bottom: 10px;
  font-family: var(--fonte-texto);
  margin-bottom: 6%;
}

.borda{
  border-right: 3px solid var(--cor-fundo-secundaria);
}

.formulario {
  flex: 1;
  max-width: 500px;
  margin-right: 16%;
  overflow: hidden;
}

form {
  background: var(--cor-fundo-secundaria);
  padding: 20px;
  border-radius: 8px;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
}

.grupo-input, .grupo-input-mensagem {
  margin-bottom: 10px;
}

.caixa-input {
  display: flex;
  gap: 10px;
  flex-direction: column;
  margin-bottom: 10px;
  color: #fff;
}

input, textarea {
  background: var(--cor-fundo);
  width: 100%;
  padding: 10px;
  border: none;
  border-radius: 5px;
  font-size: 1em;
  font-family: var(--fonte-texto);
  outline: none;
  color: #fff;
}

textarea {
  resize: none;
  margin-bottom: 3%;
  color: #fff;
}

.botao {
  background-color: var(--cor-primaria);
  color: #000;
  border: none;
  padding: 10px 15px;
  cursor: pointer;
  font-size: 1em;
  border-radius: 5px;
  transition: background 0.3s;
}

.botao:hover {
  background-color: var(--cor-secundaria);
}

/* Responsividade */
@media (max-width: 768px) {
  .conteudo-contato {
    flex-direction: column;
    align-items: center;
    text-align: center;
  }

  .informacoes-contato {
    display: none;
  }

  .formulario {
    align-items: center;
    justify-content: center;
    margin: 5% 10%;
    order: 1; /* Define a ordem para aparecer primeiro */
  }

  .borda {
    display: none;
  }

  .caixa-input {
    flex-direction: column;
  }
}

@media (max-width: 480px) {
  .titulo {
    font-size: 2em;
  }

  .descricao {
    width: 90%;
    margin: 0 auto;
    text-align: center;
    font-size: 1em;
  }

  input, textarea {
    font-size: 0.9em;
    padding: 8px;
  }

  .botao {
    font-size: 0.9em;
    padding: 8px;
  }
}
</style>