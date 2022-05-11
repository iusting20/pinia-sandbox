<script setup>
import { useCounterStore } from "@/stores/counter";
import Counter from "@/components/Counter.vue";

const storeCounter = useCounterStore();
</script>

<template>
  <div class="home">
    <Counter></Counter>
    <div class="buttons">
      <button @click="storeCounter.decrement()">-</button>
      <button @click="storeCounter.increment()">+</button>
    </div>

    <hr />

    <div class="text">This counter is {{ storeCounter.oddOrEven }}</div>

    <hr />

    <div class="editCouter">
      <b>Edit the counter:</b>
      <br />
      <input type="number" v-model="storeCounter.count" />
    </div>
  </div>
</template>

<style>
.count {
  font-size: 60px;
  margin: 20px;
}

.buttons button {
  font-size: 40px;
  margin: 10px;
}
</style>
