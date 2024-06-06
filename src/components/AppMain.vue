<script>
import OurSolutions from "./AppMainComponents/OurSolutions.vue";
import OurMissions from "./AppMainComponents/OurMissions.vue";
import OurPrices from "./AppMainComponents/OurPrices.vue";
import ClientsQuotes from "./AppMainComponents/ClientsQuotes.vue";
import OurResults from "./AppMainComponents/OurResults.vue";
import OurWorks from "./AppMainComponents/OurWorks.vue";
import LatestNews from "./AppMainComponents/LatestNews.vue";
import NewProjects from "./AppMainComponents/NewProjects.vue";

export default {
	name: "AppMain",
	components: {
		OurMissions,
		OurSolutions,
		OurPrices,
		ClientsQuotes,
		OurResults,
		OurWorks,
		LatestNews,
		NewProjects,
	},
};
</script>

<template>
	<div class="box">
		<OurSolutions />
	</div>

	<OurMissions />

	<div class="box">
		<OurWorks />
	</div>

	<OurResults />

	<div class="box">
		<OurPrices />
	</div>

	<ClientsQuotes />

	<div class="box">
		<LatestNews />
	</div>

	<NewProjects />
</template>

<style scoped></style>
