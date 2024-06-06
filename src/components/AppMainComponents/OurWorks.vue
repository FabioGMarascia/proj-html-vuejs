<script>
export default {
	name: "OurWorks",
	data() {
		return {
			urlPhotoCard: [
				"ina-soulis-227104-unsplash-1024x1024.jpg",
				"sunisa-misa-531163-unsplash-1024x1024.jpg",
				"355H-1024x1024.jpg",
				"photo-1448932252197-d19750584e56-1024x1024.jpg",
				"business-competition-PB366D8-1024x1024.jpg",
				"cozy-sofa-in-living-room-PQR5AB9-1024x1024.jpg",
				"aa9a4539-PQGJ7HU-1024x1024.jpg",
				"cody-davis-253928-unsplash-1024x1024.jpg",
			],
		};
	},
	methods: {
		getImg(path) {
			let risultato = new URL(`../../assets/photo/` + path, import.meta.url);
			return risultato.href;
		},
	},
	mounted() {},
};
</script>

<template>
	<section id="ourWorks" class="mb-5">
		<div class="row">
			<div class="col-5 m-0 debug px-0">
				<hr class="d-inline-block me-2 rounded bg-success opacity-100" />

				<hr class="separator d-inline-block rounded bg-success opacity-100" />

				<p class="fw-bold pt-4 display-4">
					Our recent <span>web designs</span> & some examples of past <span>projects</span>
				</p>

				<hr class="d-inline-block me-2 rounded bg-success opacity-100" />

				<hr class="separator d-inline-block rounded bg-success opacity-100" />
			</div>

			<div class="col-7 py-5 ps-5 d-flex flex-column-reverse p-0 m-0 debug">
				<p class="px-0">
					Far Far away, behind the word mountains, Far From the countries Vokalie end
					Consonentia, there live the blind texts. Seperated they live in Bookmarksgrove righi
					the coesi: OF the Semantics, è large languege ocean.Separated they live in
					Bookmarksgrove.Far far away, behind the word mountèins, far From the countries
					Vokalia and Consonentia, there live the blind texts. Separated they live in
					Bookmarksgrave.
				</p>
			</div>
		</div>
	</section>

	<section>
		<div class="row mx-0">
			<div v-for="url in urlPhotoCard" class="card border-0 g-1 col-3 h-100 position-relative">
				<img :src="getImg(url)" class="card-img w-100" />
				<div class="card-img-overlay cardTextBox text-white ps-5 align-content-end pb-5">
					<h4>The Basket of Flowers</h4>

					<span>BRANDING</span>

					<i class="fa-solid fa-circle fa-2xs mx-2"></i>

					<span>MARKETING</span>
				</div>
			</div>
		</div>
	</section>

	<section>
		<div class="row p-5 m-5 mx-0">
			<div class="col-12 m-3 text-center">
				<button class="btn rounded-5 text-white px-5 py-3 shadow-lg mt-4 fs-6">
					<div class="background"></div>
					READ MORE
				</button>
			</div>
		</div>
	</section>
</template>

<style scoped>
#ourWorks {
	padding-top: 10rem;
}

button {
	background-color: rgb(134, 206, 117);
}
span {
	color: white;
}

button {
	font-size: 0.6rem;
	display: inline-block;
	position: relative;
	background-color: #d5c264;
	transition: color 0.5s;
	z-index: 1;
	overflow: hidden;
}

.cardTextBox {
	opacity: 0;
	background: linear-gradient(
		271deg,
		rgba(122, 222, 108, 0.8) 0%,
		rgba(88, 221, 125, 0.8) 60%,
		rgba(0, 217, 166, 0.8) 100%
	);
}

.cardTextBox:hover {
	opacity: 1;
}

.card:hover {
	scale: 1.1;
	transition: 0.5s;
	z-index: 3;
}

.background {
	width: 0;
	height: 0;
	position: absolute;
	top: 50%;
	left: 50%;
	transform: translate(-50%, -50%);
	transition: 0.5s;
	z-index: -1;
	border-radius: 50%;
	background: linear-gradient(
		271deg,
		rgba(65, 65, 65, 1) 0%,
		rgba(47, 47, 47, 1) 50%,
		rgba(18, 20, 19, 1) 100%
	);
}

button:hover .background {
	width: 150%;
	height: 400%;
}

hr,
.separator,
button,
.bgImg {
	background: linear-gradient(
		271deg,
		rgba(122, 222, 108, 1) 0%,
		rgba(88, 221, 125, 1) 60%,
		rgba(0, 217, 166, 1) 100%
	);
}

p span {
	color: #00d9a6;
}
</style>
