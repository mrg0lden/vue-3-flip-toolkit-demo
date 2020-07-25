<template>
	<div class="flex flex-col items-center">
		<img
			alt="Vue logo"
			src="./assets/logo.png"
		/>
		<HelloWorld msg="Hello Vue 3.0 + Vite" />
	</div>
</template>

<script lang="ts">
import HelloWorld from "./components/HelloWorld.vue";
import { defineComponent } from "vue";

export default defineComponent({
	name: "App",
	components: {
		HelloWorld,
	},
});
</script>
