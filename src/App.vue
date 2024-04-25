<template>
  <Navbar v-bind:titulonav="titulo"  v-bind:servicionav="servicios"/>
  <div class="container mt-4">
    <!-- <h1>{{ saldo }}</h1> -->

    <Table v-bind:saldoTable="saldo"/>

    <button v-on:click="agregarSaldo" class="btn btn-success mx-2">Aumentar Saldo</button>
    <button v-on:click="disminuirSaldo" class="btn btn-danger">Disminuir Saldo </button>

    <!-- <a v-bind:href="url">Ir Github</a> -->
  </div>
</template>

<script>
import Navbar from './components/Navbar.vue'
import Table from './components/Table.vue'

export default {
  name: 'App',
  components: {
    Navbar,
    Table
  },
  data() {
    return {
      saldo: 0,
      titulo: "BancoVue",
      servicios: ['Prestamos', 'Cuenta Corriente', 'Giros', 'Depositos'],
      url: "https://www.github.com"
    }
  },
  methods: {
    agregarSaldo() {
      this.saldo = this.saldo + 1;
    },
    disminuirSaldo() {
      this.saldo = this.saldo - 1;
    }
  
  }
}
</script>

<style></style>