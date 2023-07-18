<template>
	<template v-if="state == 'menu'">
		<h3>Galaxy Raiders</h3>
		<button @click="state = 'game'">Jogar</button>
		<button @click="state = 'leaderboard'">Placar</button>
		<button @click="close()">Fechar</button>
	</template>
	<template v-if="state == 'leaderboard'">
		<Leaderboard />
		<button @click="state = 'menu'">Back to menu</button>
	</template>
	<template v-if="state == 'game'">
		<Game />
	</template>
</template>

<script setup>
import { ref } from 'vue'

const state = ref('menu')

</script>

<script>
export function close() {
	alert("Fechando...\n(Não implementado)")
}
</script>

<style>
</style>
