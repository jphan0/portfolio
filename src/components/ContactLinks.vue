<template>

	<div class="text-center">
		
		<a href="https://www.linkedin.com/in/jphan0/">LinkedIn</a>

		<span id="divider">||</span>

		<a href="mailto:jphan@sent.com">jphan@sent.com</a>

		<span id="divider">||</span>

		<a href="https://www.github.com/">GitHub</a>

	</div>



</template>



<script>

export default {

}

</script>



<style scoped>

div {
	padding-top: 50px;
	padding-bottom: 100px;

}

a {
	padding: 40px;
	display: inline-block;
	position: relative;
    text-decoration: none;
    color: #5a5d7a;
}

a:hover {
	text-decoration: none;
	color: black;
}

a:before {
	content: "";
	position: absolute;
	width: 50%;
	height: 2px;
	bottom: 35px;
	left: 26%;
	transform: translate(-50%);
	background-color: #5a5d7a;
	visibility: hidden;
	-webkit-transform: scaleX(0);
	transform: scaleX(0);
	-webkit-transition: all 0.3s ease-in-out 0s;
	transition: all 0.3s ease-in-out 0s;
}

a:hover:before {
	visibility: visible;
	-webkit-transform: scaleX(1);
	transform: scaleX(1);
}

@media screen and (max-width: 768px) {

	#divider {
		display: none;
	}

	a {
		padding: 10px;
	}
}


</style>
