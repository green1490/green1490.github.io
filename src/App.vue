<script setup lang="ts">
	import Navbar from './components/Navbar.vue'
	import Home from './components/Home.vue'
	import About from './components/About.vue'
</script>

<template>
	<Navbar/>
	<Transition name="bounce">
		<RouterView/>
	</Transition>
</template>

<style>
	.bounce-enter-active {
  		animation: bounce-in 0.5s;
	}
	
	.bounce-leave-active {
		animation: bounce-in 0.5s reverse;
	}
	
		@keyframes bounce-in {
		0% {
			transform: scale(0);
		}
		50% {
			transform: scale(1.25);
		}
		
		100% {
			transform: scale(1);
		}
	}
</style>