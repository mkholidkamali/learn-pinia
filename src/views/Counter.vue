<script setup lang="ts">
import { useCounterStore } from "@/stores/counter";
import { storeToRefs } from "pinia";

const counterStore = useCounterStore();
const { count, doubleCount } = storeToRefs(counterStore)
</script>

<template>
	<div>
		<p>Count: {{ count }}</p>
		<p>Double Count: {{ doubleCount }}</p> 
		<button @click="counterStore.decrement">Decrement</button>
		<button @click="counterStore.increment">Increment</button>
	</div>
</template>
