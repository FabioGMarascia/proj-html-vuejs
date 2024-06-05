<script>
import OurSolutions from "./AppMainComponents/OurSolutions.vue";
import OurMissions from "./AppMainComponents/OurMissions.vue";
import OurPrices from "./AppMainComponents/OurPrices.vue";
import ClientsQuotes from "./AppMainComponents/ClientsQuotes.vue";
import OurResults from "./AppMainComponents/OurResults.vue";

export default {
	name: "AppMain",
	components: {
		OurMissions,
		OurSolutions,
		OurPrices,
		ClientsQuotes,
		OurResults,
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

	<ClientsQuotes />

	<OurResults />
</template>

<style scoped>
.box {
	margin: 0 10rem;
}
</style>
