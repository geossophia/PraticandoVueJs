<script>
export default {
  props: {
    nome: String,
    apelido: String,
    turma: String,
  },
};
</script>
<template>
  <section class="card">
    <h2 class="name">{{ nome }}</h2>
    <h2 class="apelido">({{ apelido }})</h2>
    <h3 class="turma">Turma: {{ turma }}</h3>
  </section>
</template>
<style>
.card {
  width: 17em;
  margin: 2em;
  border-radius: 0.8em;
  height: 13em;
  border: 2px solid rgb(58, 160, 185);
  box-shadow: 0 0 16px 0 rgb(0 0 0 / 17%);
}
.apelido,
.name {
  display: flex;
  justify-content: center;
  padding-top: 1em;
}
.apelido {
  padding: 0;
  font-size: 1rem;
}
.turma {
  padding-top: 0.9em;
}
h3 {
  margin-left: 1em;
}
.button-59 {
  align-items: center;
  background-color: #fff;
  border: 2px solid #000;
  box-sizing: border-box;
  color: #000;
  cursor: pointer;
  display: inline-flex;
  fill: #000;
  font-family: Inter,sans-serif;
  font-size: 16px;
  font-weight: 600;
  height: 48px;
  justify-content: center;
  letter-spacing: -.8px;
  line-height: 24px;
  min-width: 140px;
  outline: 0;
  padding: 0 17px;
  text-align: center;
  text-decoration: none;
  transition: all .3s;
  user-select: none;
  -webkit-user-select: none;
  touch-action: manipulation;
}

.button-59:focus {
  color: #171e29;
}

.button-59:hover {
  border-color: #06f;
  color: #06f;
  fill: #06f;
}

.button-59:active {
  border-color: #06f;
  color: #06f;
  fill: #06f;
}

@media (min-width: 768px) {
  .button-59 {
    min-width: 170px;
  }
}
</style>
