<template>

<div class="jumbotron jumbotron bg-cover">

<div class="logo">

	<a href="http://jphan.info"><img src="~@/assets/img/logo.png" height="40px"></a>

</div>

<div class="navigation">

	<a href="#projects" v-scroll-to="'#projects'">Projects</a>

	<a href="#contact" v-scroll-to="'#contact'">Contact</a>

</div>


<div class="overlay"></div>

	<div class="container">

		<img class="profile-image" src="~@/assets/img/head.jpg"/>

		<h1 class="display-3"> {{ mainheading }} </h1>

		<h3> {{ subtext }} </h3>

		<div class="icons text-center"> 

			<span class="devicons devicon-html5-plain" title="HTML5"></span>

			<span class="devicons devicon-css3-plain" title="CSS3"> </span>

			<span class="devicons devicon-sass-original" title="SCSS"></span>

			<span class="devicons devicon-javascript-plain" title="JavaScript"></span>

			<span class="devicons devicon-laravel-plain" title="Laravel"></span>

			<span class="devicons devicon-vuejs-plain" title="VueJS"></span>

			<span class="devicons devicon-git-plain" title="git"> </span>

		</div>

		<div class="scroll-down text-center">

			<a href="#projects" v-scroll-to="'#projects'"><i class="fas fa-chevron-down fa-2x"></i></a>

		</div>

	</div>

</div>

</template>



<script>

export default {

  props: ["mainheading", "subtext"],

}

</script>



<style scoped>

@import url('https://fonts.googleapis.com/css?family=Cormorant+Garamond:300,400,700');
@import url("https://fonts.googleapis.com/css?family=Montserrat:300,400,700,800");

h1 {
	font-family: 'Cormorant Garamond', serif;
	padding-top: 20px;
	font-weight: 300;
}

h3 {
	font-family: 'Montserrat', helvetica, arial, sans-serif;
	font-size: 1.3em;
	font-weight: 300;
	color: #E3E3E3;
	opacity: 0.85;
	padding-top: 30px;
	line-height: 1.5em;
}

h1, h3 {
	
	padding-left: 100px;
	padding-right: 100px;
}

a {
	position: relative;
	font-family: 'Montserrat', helvetica, arial, sans-serif;
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
	padding-top: 5vh;
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

.bg-cover {
    background-image: url('~@/assets/img/nature-2.jpg');
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
}

.icons span {
	padding: 10px;
	font-size: 3em;
	margin: 0px 6px;
	opacity: 0.8;
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


@media screen and (max-width: 768px) {

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

	h1, h3 {
		padding: 5px;
	}

	.icons span {
		padding: 2px;
		font-size: 2em;
		margin: 0px 6px;
		opacity: 0.6;
	}
}

@media screen and (min-height: 900px) {
	.jumbotron {
		min-height: 50vh;
	}
}

</style>
