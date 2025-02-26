<script setup lang="ts">
import { useCounterStore } from "@/stores/counter";

const counterStore = useCounterStore();
</script>

<template>
	<div>
		<p>Count: {{ counterStore.count }}</p>
		<p>Double Count: {{ counterStore.doubleCount }}</p> 
		<button @click="counterStore.decrement">Decrement</button>
		<button @click="counterStore.increment">Increment</button>
	</div>
</template>