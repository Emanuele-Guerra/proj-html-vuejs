<script>
import AppHeader from "./components/AppHeader.vue"
import AppConsultant from "./components/AppConsultant.vue";
import AppMain from "./components/AppMain.vue";
import AppMainSecond from "./components/AppMainSecond.vue";
import AppPreFooter from "./components/AppPreFooter.vue";
import AppFooter from "./components/AppFooter.vue"
import { store } from "./store.js" //state management

export default {
	components: {

		AppHeader,
		AppConsultant,
		AppMain,
		AppMainSecond,
		AppPreFooter,
		AppFooter
	},
	data() {
		return {
			store
		}
	},
	mounted() {
		this.doThings();

		// axios.get("indirizzo").then(risultato => {
		// 	console.log(risultato);
		// }).catch(errore => {
		// 	console.error(errore);
		// });
	},
	methods: {
		doThings() {
			console.log("App.vue does things");
		}
	}
}
</script>

<template>
	<header>
		<AppHeader />
		<img src="public/portrait-of-young-architect-woman-on-meeting-KFZCE3A.jpg" alt="">
		<div class="jumbo-container">
			<div class="flexed-head">
				<div class="square"></div>
				<h3>ALWAYS THE BEST WAY YOU NEED IT</h3>
			</div>
			<h1>THE BEST BUSINESS CONSULTING</h1>
			<div class="flexed">
				<button>READ MORE</button>
				<div class="play">
					<i class="fa-sharp fa-solid fa-play"></i>
				</div>
			</div>



		</div>
	</header>
	<main>
		<AppConsultant />
		<AppMain />
		<AppMainSecond />
		<AppPreFooter />
		<AppFooter />


	</main>
</template>

<style lang="scss">
// importo il foglio di stile generale dell'applicazione, non-scoped
@use './styles/general.scss';
</style>

<style scoped lang="scss">
// importo variabili
// @use './styles/partials/variables' as *;

// ...qui eventuale SCSS di App.vue

body {
	position: relative;
}

header {
	width: 100%;
	color: white;

	img {
		position: absolute;
		right: 0;
		top: 0;
		z-index: -2;
		width: 1070px;
	}
}

.jumbo-container {
	margin: 270px 0 0 2.5rem;
	width: 600px;

	h3 {
		font-size: 20px;
		font-weight: 50;
		letter-spacing: 2.8px;

	}

	h1 {
		font-size: 100px;
		line-height: 90px;
	}

	button {
		padding: 1.5rem 3rem;
		background-color: #39FFBF;
		border: none;
		font-size: 16px;
	}
}

.flexed-head {
	display: flex;
	align-items: center;
	margin-bottom: 1rem;
}

.flexed {
	margin-top: 3rem;
	display: flex;
	align-items: flex-end;
}

.square {
	width: 50px;
	height: 3px;
	background-color: #39FFBF;
	display: inline-block;
	margin-right: 1rem;
}

.play {
	display: inline-block;
	display: flex;
	justify-content: center;
	align-items: center;
	height: 3.3rem;
	width: 3.3rem;
	border-radius: 50%;
	border: 2px solid white;
	margin: 0 2rem;
}
</style>