<script>
export default {
	name: "OurSolutions",
	components: {},
};
</script>

<template>
	<div class="ourSolBox row mx-0">
		<div class="ourSolBoxLeft col-4 ps-0 mt-5">
			<p class="fw-bold py-4 display-4">
				We Are Here To Make Your <span class="text-success">Website</span> Look More
				<span class="text-success">Elegant</span> And Stylish!
			</p>

			<hr class="d-inline-block me-2 rounded bg-success opacity-100" />

			<hr class="separator d-inline-block rounded bg-success opacity-100" />

			<div>
				<button class="btn bg-success rounded-5 text-white px-5 py-3">VIEW ALL</button>
			</div>
		</div>

		<div class="ourSolBoxRight col-8">
			<div class="row gap-5 justify-content-end">
				<div class="col-5 p-5 border border-1 border-secondary-emphasis rounded shadow">
					<i class="fa-solid fa-gauge-simple-high fs-1"></i>
					<h2 class="my-4">Speed Optimization</h2>
					<p>
						Far far away, behind the word mountains, far from the countries Vokalia
						Separated...
					</p>
				</div>

				<div class="col-5 p-5 border border-1 border-secondary-emphasis rounded shadow">
					<i class="fa-solid fa-cloud fs-1"></i>
					<h2 class="my-4">Cloud Solutions</h2>
					<p>
						Far far away, behind the word mountains, far from the countries Vokalia
						Separated...
					</p>
				</div>

				<div class="col-5 p-5 border border-1 border-secondary-emphasis rounded shadow">
					<i class="fa-solid fa-tablet-screen-button fs-1"></i>
					<h2 class="my-4">Website Design</h2>
					<p>
						Far far away, behind the word mountains, far from the countries Vokalia
						Separated...
					</p>
				</div>

				<div class="col-5 p-5 border border-1 border-secondary-emphasis rounded shadow">
					<i class="fa-solid fa-stopwatch fs-1"></i>
					<h2 class="my-4">Online Marketing</h2>
					<p>
						Far far away, behind the word mountains, far from the countries Vokalia
						Separated...
					</p>
				</div>
			</div>
		</div>
	</div>
</template>

<style scoped>
hr {
	width: 0.8rem;
	padding: 0.2rem 0;
}

.separator {
	width: 3rem;
	padding: 0.2rem 0;
}

button {
	font-size: 0.6rem;
}
</style>
