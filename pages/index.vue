<template>
  <div>
    <form @submit.prevent="receberNome">
      <input v-model="inputNome" type="text" name="" id="">
      <button> Adicionar </button>
    </form>
    <ul>
      <li v-for="nome in nomes"> {{ nome }}</li>
    </ul>
  </div>
    
</template>

<script>
export default {
  data() {
    return {
      InputNome: "",
      nomes: []
    }
  },
  methods: (
    receberNome() {
      this.nomes.push(this.inputNome)
      this.inputNome = "";
    }
  )
}
</script>
