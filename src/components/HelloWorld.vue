<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    {{ numero }} 
    <button @click="incrementar()">+ Incrementar</button>
    <h1 v-if="numero<=2">
      Texto 1
    </h1>
    <h1 v-else>
      Texto 2
    </h1>
    <ul>
      <li v-for="(herramientas, indice) in herramientas" :key="indice">
      {{ indice }}-{{ herramientas }}
      </li>
    </ul>
    <input :type="tiipo" placeholder="Escribe aqui" v-model="texto">
    <h1>{{ texto }}</h1>
    <button @click="cambiarinput()">passord/texto</button>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data() {
    return {
      numero: 1,
      herramientas:[
        "Alicate",
        "Destornillador",
        "Juego de llaves",
        "Destornillador"
      ],
      texto:"",
      tiipo:"password",
    }
  },
  methods: {
    incrementar(){
      this.numero++;
    },
    cambiarinput(){

      this.tiipo = this.tiipo === "password" ? 'text' : 'password';
      
    },
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
