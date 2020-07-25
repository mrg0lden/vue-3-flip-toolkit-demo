<template>
	<div class="flex flex-col">
		<h1 class>{{ msg }}</h1>
		<button
			@click="expand = !expand"
			class="btn"
		>Flip it!</button>
		<flipper :flip-key="expand">
			<flipped flip-id="flipping-sqaure">
				<div
					:class="{'active': expand}"
					class="box"
				></div>
			</flipped>
		</flipper>
	</div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import { Flipper, Flipped } from "vue-flip-toolkit";
export default defineComponent({
	name: "HelloWorld",
	components: {
		Flipper,
		Flipped,
	}, 
	props: {
		msg: String,
	},
	data() {
		return {
			expand: true,
		};
	},
});
</script>
<style lang="postcss">
.btn {
	@apply bg-gray-800 text-gray-300 py-2 px-3 rounded;
}

.box {
	@apply bg-red-600 w-12 h-40;
	&.active {
		@apply w-24 h-32;
	}
}
</style>