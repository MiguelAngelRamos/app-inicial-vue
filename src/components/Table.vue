<template>
<table class="table">
  <thead>
    <tr>
      <th scope="col">Saldo</th>
      <th scope="col">Estado</th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td v-bind:class="colorSaldo">{{ saldoTable }}</td>
      <td>@mdo</td>
    </tr>
 

  </tbody>
</table>
</template>


<script>
export default {
  props: {
    saldoTable: Number
  },
  computed: {
    colorSaldo() {
      return this.saldoTable >= 0 ? 'text-success': 'text-danger';
    }
  }
}
</script>

<style>
</style>