<template>
  <vs-card>
    <template v-slot:header>
      <h2>{{ expense.name }}</h2>
    </template>

    <p>Lugar de compra: {{ expense.shop_place }}</p>
    <p>Gasto: {{ expense.type }}</p>
    <div>
      <p>Total de pagos: {{ expense.partial_deadline }}</p>
      <p>Tipo de pago: {{ expense.payment_type }}</p>
      <p>Pago parcial: {{ expense.partial_to_pay }}</p>
    </div>
    <vs-checkbox v-model="expense.paid">Estatus</vs-checkbox>
  </vs-card>
</template>

<script>
export default {
  props: {
    expense: Object,
  },
  setup(props) {
    const { expense } = props;

    return {
      expense,
    };
  },
};
</script>

<style>
</style>