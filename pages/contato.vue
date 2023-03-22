<template>
    <h1> Página de Contato </h1>
    <FormularioContato @enviarDados="receberDados"
    />
    <hr>
    <p> Lista de contatos: </p>
    <ul v-for="ct in Object.keys(listaContato)">
        <li> Nome: <strong> {{ listaContato[ct].nome }}</strong></li>
        <li> Email: <strong> {{ listaContato[ct].email }}</strong></li>
        <li> Msg: <strong> {{ listaContato[ct].msg }}</strong></li>
    </ul>
</template>

<script>

export default {
    data() {
        return {
            listaContato: [
            ]
        }
    },
    methods: {
        receberDados(dados) {
            console.log(dados)
            this.listaContato.push(dados)
        }
    }
}


</script>
