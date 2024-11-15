<template>
	<div id="app">
		<span>
			<button class="vermelho" @click="setVermelho()">Carregar Componente Vermelho</button>
			<button class="verde" @click="setVerde()">Carregar Componente Verde</button>
			<button class="azul" @click="setAzul()">Carregar Componente Azul</button>
		</span>
		
		<Vermelho v-if="vermelho">Conteúdo do Componente <strong>Vermelho</strong></Vermelho>
		<Verde v-if="verde">Conteúdo do Componente <strong>Verde</strong></Verde>
		<Azul  v-if="azul">Conteúdo do Componente <strong>Azul</strong></Azul>
	
	</div>
</template>

<script>
import Vermelho from "./components/Vermelho.vue";
import Verde from "./components/Verde.vue";
import Azul from "./components/Azul.vue";

export default {
  name: "app",
  components: { Vermelho, Verde, Azul },
  data() {
    return {
      vermelho: false,
      verde: false,
      azul: false,
    };
  },
  methods: {
    setVermelho() {
      this.vermelho = true;
      this.verde = false;
      this.azul = false;
    },
    setVerde() {
      this.verde = true;
      this.vermelho = false;
      this.azul = false;
    },
    setAzul() {
      this.azul = true;
      this.vermelho = false;
      this.verde = false;
    },
  },
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

button {
  padding: 10px;
  color: #fff;
  font-size: 1.3rem;
}

.caixa {
  color: #fff;
  font-size: 1.8rem;
  padding: 25px;
  margin: 10px 0px;
}

.vermelho {
  border: 2px solid red;
  background-color: #f54235;
}

.verde {
  border: 2px solid green;
  background-color: #49b057;
}

.azul {
  border: 2px solid blue;
  background-color: #2594f0;
}
</style>
