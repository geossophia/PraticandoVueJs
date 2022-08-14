<script>
import ContatosComp from "@/components/ContatosComp.vue";
export default {
  components: {
    ContatosComp,
  },
  data() {
    return {
      nome: "Marco André",
      apelido: "peça de lego",
      situacao: "carregando...",
      turma: "2info2",
      meu_amigo: false,
      adicionados: false,
      TextoBotao: "Adicionar todos",
    };
  },
  created() {
    setTimeout(() => {
      this.situacao = "contatos";
    }, 1000);
  },
  methods: {
    Mensagem() {
      this.adicionados = !this.adicionados;
      if (!this.adicionados) {
        this.TextoBotao = "Adicionar todos";
      } else {
        this.TextoBotao = "Remover todos";
      }
    },
  },
};
</script>
<template>
  <main>
    <h2 class="contatos-h2">{{ situacao }}</h2>
    <div class="contatos-div">
      <ContatosComp nome="Isadora Goedert" :apelido="apelido" :turma="turma" />
      <ContatosComp :nome="nome" apelido="Python" turma="Sem turma" />
      <ContatosComp nome="Marcelo Harbs" apelido="poste" :turma="turma" />
      <ContatosComp nome="Greg café" apelido="sem cabelo" :turma="turma" />
      <ContatosComp
        nome="Kanye West"
        apelido="Ye"
        :turma="turma"
        v-if="meu_amigo"
      />
    </div>
    <div class="btn">
      <button @click="Mensagem" class="button-59" role="button">
        {{ TextoBotao }}
      </button>
    </div>
    <p v-if="adicionados" class="critica-social">
      todos estão adicionados nos contatos do seu celular!
    </p>
    <p v-else class="critica-social">Nem todos estão adicionados :(</p>
  </main>
</template>
<style>
.contatos-h2 {
  display: flex;
  justify-content: center;
  margin-top: 15px;
}
.btn {
  display: flex;
  justify-content: center;
  margin-bottom: 1em;
}
.contatos-div {
  display: flex;
  justify-content: space-around;
}
.critica-social {
  margin: 0 auto;
  width: 30%;
  text-align: center;
  font-size: 1.3rem;
  padding: 1em;
  margin-bottom: 1em;
  border: 2px solid rgb(58, 160, 185);
}
</style>
