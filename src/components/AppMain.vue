<script>
import OurSolutions from "./AppMainComponents/OurSolutions.vue";
import OurMissions from "./AppMainComponents/OurMissions.vue";

export default {
	name: "AppMain",
	components: {
		OurMissions,
		OurSolutions,
	},
};
</script>

<template>
	<div class="box">
		<OurSolutions />
	</div>
	<OurMissions />
</template>

<style scoped>
.box {
	margin: 0 10rem;
}
</style>
