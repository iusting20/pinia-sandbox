<script setup>
import { useCounterStore } from "@/stores/counter";

const storeCounter = useCounterStore();
</script>

<template>
  <div>
    <div class="count">{{ storeCounter.count }}</div>
  </div>
</template>
