<script>
import OurSolutions from "./AppMainComponents/OurSolutions.vue";
import OurMissions from "./AppMainComponents/OurMissions.vue";
import OurPrices from "./AppMainComponents/OurPrices.vue";

export default {
	name: "AppMain",
	components: {
		OurMissions,
		OurSolutions,
		OurPrices,
	},
};
</script>

<template>
	<div class="box">
		<OurSolutions />
	</div>

	<OurMissions />

	<div class="box">
		<OurPrices />
	</div>
</template>

<style scoped>
.box {
	margin: 0 10rem;
}
</style>
