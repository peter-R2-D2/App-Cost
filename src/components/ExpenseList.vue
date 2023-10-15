<template>
  <vs-row>
    <vs-col vs-w="12" v-for="expense of list" :key="expense.id">
      <ExpenseCard :expense="expense" />
    </vs-col>
  </vs-row>
</template>

<script>
import { ref } from 'vue';
import expenseList from "../data/expenseList.json"
import ExpenseCard from "./ExpenseCard.vue";
export default {
  components: { ExpenseCard },
  setup() {
    const list = ref(expenseList)

    return {
      list
    }
  },
};
</script>

<style>
</style>