<script>
export default {
	name: "LatestNews",
	data() {
		return {
			UrlPhoto: [
				{
					percorso: "serious-businesswoman-with-documents-talking-on-P9Q6LX6-1024.jpg",
					listitem: "Marketing Ideas",
				},

				{
					percorso: "Businessman-at-the-desk-in-his-office-resting--1024x768.jpg",
					listitem: "Rest During Hour Works",
				},
				{
					percorso: "simple-home-office-with-tree-PBXRXYB-large-1024x768.jpg",
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
				<img class="w-100 shadow-lg" :src="getImg(foto.percorso)" />
				<div class="info p-2 z-1 rounded bg-white w-75 my-0 mx-auto">
					<p>May 24.2018<i class="fa-solid fa-circle"></i> Alex</p>
					<ul>
						<li>{{ foto.listitem }}</li>
					</ul>
				</div>
			</div>
		</div>
	</section>
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
</style>
