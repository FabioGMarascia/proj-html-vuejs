<script>
export default {
	name: "LatestNews",
	data() {
		return {
			UrlPhoto: [
				{
					path: "serious-businesswoman-with-documents-talking-on-P9Q6LX6-1024.jpg",
					listitem: "Marketing Ideas",
				},

				{
					path: "Businessman-at-the-desk-in-his-office-resting--1024x768.jpg",
					listitem: "Rest During Hour Works",
				},
				{
					path: "simple-home-office-with-tree-PBXRXYB-large-1024x768.jpg",
					listitem: "Develop Your Startup Idea",
				},
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
	<section id="latestNews">
		<div class="text-center">
			<p class="fw-bold py-4 display-4">Latest News And Our <span>Blog</span></p>

			<div class="my-0 mx-auto w-25 mb-4">
				<hr class="d-inline-block me-2 rounded opacity-100" />
				<hr class="separator d-inline-block rounded opacity-100" />
			</div>
		</div>

		<div class="row mb-5 mx-0">
			<div v-for="foto in UrlPhoto" class="photo-box col overflow-hidden rounded px-0 mx-3">
				<img class="w-100 shadow-lg" :src="getImg(foto.path)" />
				<div class="info p-2 z-1 rounded bg-white w-75 my-0 mx-auto">
					<p>May 24.2018<i class="fa-solid fa-circle"></i> Alex</p>
					<ul>
						<li>{{ foto.listitem }}</li>
					</ul>
				</div>
			</div>
		</div>
	</section>

	<div class="my-5 text-center">
		<a href="">
			<button class="btn rounded-5 border-0 text-white px-5 py-3 shadow-lg mt-4 fs-6">
				<div class="background"></div>
				VIEW ALL POST
			</button>
		</a>
	</div>
</template>

<style scoped>
#latestNews {
	padding-top: 10rem;
}

.photo-box:hover img {
	scale: 1.2;
	transition: 0.5s;
}

.photo-box:hover .info {
	transition: 0.5s;
	scale: 1.1;
	color: white;
}

.photo-box:hover .info,
hr,
.separator {
	background: linear-gradient(
		271deg,
		rgba(122, 222, 108, 1) 0%,
		rgba(88, 221, 125, 1) 60%,
		rgba(0, 217, 166, 1) 100%
	);
	transition: 0.5s;
}

.info {
	position: relative;
	bottom: 40px;
}

.info:hover {
	transition: 0.5s;
	scale: 1.1;
}

img:hover {
	scale: 1.2;
	transition: 0.5s;
}
::marker {
	color: green;
	font-size: 25px;
}
p > .fa-circle {
	font-size: 4px;
	position: relative;
	bottom: 3px;
}

p span {
	color: #00d9a6;
}

button {
	font-size: 0.6rem;
	display: inline-block;
	position: relative;
	background-color: #d5c264;
	transition: color 0.5s;
	z-index: 1;
	overflow: hidden;
	background: linear-gradient(
		271deg,
		rgba(65, 65, 65, 1) 0%,
		rgba(47, 47, 47, 1) 50%,
		rgba(18, 20, 19, 1) 100%
	);
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
		rgba(122, 222, 108, 1) 0%,
		rgba(88, 221, 125, 1) 60%,
		rgba(0, 217, 166, 1) 100%
	);
}

button:hover .background {
	width: 150%;
	height: 400%;
}
</style>
