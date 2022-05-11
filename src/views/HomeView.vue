<script setup>
import { ref, computed } from "vue";
import { useCounterStore } from "@/stores/counter";

const count = ref(0);

const storeCounter = useCounterStore();

const increaseCount = () => {
  count.value++;
};

const decreaseCount = () => {
  count.value--;
};
</script>

<template>
  <div class="home">
    <div class="count">{{ storeCounter.count }}</div>
    <div class="buttons">
      <button @click="storeCounter.decrement()">-</button>
      <button @click="storeCounter.increment()">+</button>
    </div>

    <hr />

    <div class="text">This counter is {{ storeCounter.oddOrEven }}</div>
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
