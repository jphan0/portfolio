<template>

<div class="jumbotron jumbotron bg-cover">

<div class="logo">

	<a href="https://jphan.info">

		<picture>

			<source type="image/webp" class="site-logo" srcset="~@/assets/img/logo.webp">

			<source type="image/jpeg" class="site-logo" srcset="~@/assets/img/logo.png">

			<img src="~@/assets/img/logo.png" class="site-logo" alt="logo">

		</picture>

	</a>

</div>

<div class="navigation">

	<a href="#projects" v-scroll-to="'#projects'">Projects</a>

	<a href="#contact" v-scroll-to="'#contact'" @click.ctrl="say('This is a little easter egg. Hello!')">Contact</a>

</div>


<div class="overlay"></div>

	<div class="container">

		<picture>

			<source type="image/webp" srcset="~@/assets/img/head.webp">

			<source type="image/jpeg" srcset="~@/assets/img/head.jpg">

			<img class="profile-image" src="~@/assets/img/head.jpg" alt="head image">

		</picture>

		<h1 class="display-3"> {{ mainheading }} </h1>

		<h3> {{ subtext }} </h3>

		<div class="icons text-center"> 

			<img src="../assets/img/devicon/html5.svg" title="HTML5" alt="HTML5">

			<img src="../assets/img/devicon/css3.svg" title="CSS3" alt="CSS3">

			<img src="../assets/img/devicon/sass.svg" title="SCSS" alt="SCSS">

			<img src="../assets/img/devicon/javascript.svg" title="JavaScript" alt="JavaScript">

			<img src="../assets/img/devicon/laravel.svg" title="Laravel" alt="Laravel">

			<img src="../assets/img/devicon/vuejs.svg" title="VueJS" alt="VueJS">

			<img src="../assets/img/devicon/git.svg" title="git" alt="git">

		</div>

		<div class="scroll-down text-center">

			<a href="#projects" v-scroll-to="'#projects'"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="#FFFFFF"><path d="M0 7.33l2.829-2.83 9.175 9.339 9.167-9.339 2.829 2.83-11.996 12.17z"/></svg></a>

		</div>

	</div>

</div>

</template>



<script>

export default {

	methods: {
		
		say: function (message) {
		
			alert(message)
		
		}
	
	},

	props: ["mainheading", "subtext"],

}

</script>



<style scoped>

.site-logo {
	position: absolute;
	max-height: 150%;
}

h1 {
	font-family: 'Cormorant Garamond', helvetica, arial, sans-serif;
	padding-top: 20px;
	font-weight: 300;
}

h3 {
	font-size: 1.3em;
	font-weight: 300;
	color: #E3E3E3;
	opacity: 0.9;
	padding-top: 30px;
	line-height: 1.5em;
}

h1, h3 {
	
	padding-left: 100px;
	padding-right: 100px;
}

a {
	position: relative;
	font-weight: 300;
	text-decoration: none;
	color: #E3E3E3;
	font-size: 1.5em;
	padding-left: 40px;
	padding-right: 40px;
}

.navigation a:hover {
	text-decoration: none;
	color: white;
}

.navigation a:before {
	content: "";
	position: absolute;
	width: 50%;
	height: 2px;
	bottom: -7px;
	left: 40px;
	background-color: white;
	visibility: hidden;
	-webkit-transform: scaleX(0);
	transform: scaleX(0);
	-webkit-transition: all 0.3s ease-in-out 0s;
	transition: all 0.3s ease-in-out 0s;
}

.navigation a:hover:before {
	visibility: visible;
	-webkit-transform: scaleX(1);
	transform: scaleX(1);
}

.logo {
	position: absolute;
	top: 40px;
	left: 80px;
}

.navigation {
	position: absolute;
	top: 40px;
	right: 80px;
}

.container {
	padding-top: 10vh;
}

.profile-image {
	border-radius: 50%;
	width: 160px;
	height: 160px;
	border: 3px solid #ddd;
	z-index: 1;
}

.jumbotron {
	text-align: center;
	padding-top: 10rem;
	padding-bottom: 10rem;
	text-shadow: 1px 1px 5px #000;
	min-height: 100vh;
}

.no-webp .bg-cover {
  background-image: url("~@/assets/img/nature-2.jpg");
}

.webp .bg-cover{
  background-image: url("~@/assets/img/nature-2.webp");
}

.bg-cover {
	background-size: cover;
	color: white;
	background-position: center center;
	position: relative;
	z-index: 0;

}

.overlay {
	background-color: #000;
	opacity: 0.5;
	position: absolute;
	top: 0;
	left: 0;
	bottom: 0;
	right: 0;
	z-index: -1;
}

.icons {
	padding-top: 50px;
	text-shadow: 2px 2px 4px #000000;
}

.icons img {
	padding: 10px;
	width: 7vh;
	margin: 0px 6px;
	opacity: 0.7;
	-webkit-filter: brightness(0) invert(1);
	filter: brightness(0) invert(1);
}

.scroll-down a {
	position: absolute;
	left: 0;
	right: 0;
	margin: auto;
	bottom: 30px;
	opacity: 0.8;
	-webkit-animation-duration: 2s;
	animation-duration: 2s;
	-webkit-animation-fill-mode: both;
	animation-fill-mode: both;
	-webkit-animation-timing-function: ease-in-out;
	animation-timing-function: ease-in-out;
	animation-iteration-count: infinite;
	-webkit-animation-iteration-count: infinite;
	color: white;
}

.scroll-down a:hover {
	cursor: pointer;
	animation-name: bounce;
	-moz-animation-name: bounce;
}

@keyframes bounce {
	0%, 100%, 20%, 50%, 80% {
		-webkit-transform: translateY(0);
		-ms-transform:     translateY(0);
		transform:         translateY(0)
	}
	40% {
		-webkit-transform: translateY(-25px);
		-ms-transform:     translateY(-25px);
		transform:         translateY(-25px)
	}
	60% {
		-webkit-transform: translateY(-15px);
		-ms-transform:     translateY(-15px);
		transform:         translateY(-15px)
	}
}

@media screen and (max-width: 767px) {
	.jumbotron {
		max-height: 100vh;
	}

	.logo {
		display: none;
	}

	.container {
		padding-top: 0;
	}

	a {
		position: relative;
		padding: 30px;
	}

	.navigation {
		left: 0;
		right: 0;
	}

	.navigation a:hover:before {
		visibility: hidden;
	}

	h1{
		font-size: 4em;
		padding: 5px;

	}

	h3 {
		font-size: 1.2em;
		padding: 5px;
	}

	.icons {
		padding-top: 10px;
	}

	.icons img {
		padding-top: 10px;
		width: 7vh;
		margin: 0px 6px;
	}

	.scroll-down a {
		bottom: -15px;
	}
}


@media screen and (min-height: 1300px) {
	.jumbotron {
		min-height: 50vh;
	}

	h1{
		font-size: 5em;
		padding: 5px;

	}

	h3 {
		font-size: 1.6em;
		padding: 5px;
	}

	.icons img {
	width: 4vh;
	}

	.container {
		padding-top: 5vh;
	}
}

</style>
