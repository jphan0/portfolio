<template>

<h2 class="text-center"> {{ heading }} </h2>

</template>



<script>

export default {

  props: ["heading"],

}

</script>

<style scoped>

h2 {
	padding-top: 50px;
	text-decoration: none; 
    position: relative; 
}

h2:after {
    position: absolute;
    content: '';
    height: 2px;
    bottom: -10px; 
	margin: 0 auto;
	left: 0;
	right: 0;
	width: 5%;
	background: darkgrey;
	-o-transition:.5s;
	-ms-transition:.5s;
	-moz-transition:.5s;
	-webkit-transition:.5s;
	transition:.5s;
}

h2:hover:after {
	width: 7%;
	background: orange;
    }

@media screen and (max-width: 768px) {
  h2:after {
    width: 30%;
  }

  h2:hover:after {
	width: 35%;
  }
}



</style>
