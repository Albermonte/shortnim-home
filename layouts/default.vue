<template>
	<div class="background-gradient">
		<Header />
		<transition
			name="fade"
			mode="out-in"
		>
			<Nuxt />
		</transition>
	</div>
</template>

<script>
import Header from "@/components/Header";
export default {
	components: {
		Header,
	},
};
</script>

<style>
.background-gradient {
	background-image: linear-gradient(#265dd7, #0582ca);
}

.fade-enter-active,
.fade-leave-active {
	transition-duration: 0.3s;
	transition-property: opacity;
	transition-timing-function: ease;
}

.fade-enter,
.fade-leave-active {
	opacity: 0;
}
</style>
