<template>
	<ol>
		<li v-for="score in leaderboard">
			{{score["timestamp"]}}: {{score["score"]}}
		</li>
	</ol>
</template>

<script setup>
import { ref } from 'vue'

// change here to get leaderboard from server
const leaderboard = ref([{"timestamp":1689371592,"score":8150.0},{"timestamp":1689675464,"score":4200.0},{"timestamp":1689678006,"score":400.0}])
</script>

<style scoped>
</style>
