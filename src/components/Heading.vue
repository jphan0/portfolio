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
	width: 7vw;
	background: darkgrey;
	-o-transition:.5s;
	-ms-transition:.5s;
	-moz-transition:.5s;
	-webkit-transition:.5s;
	transition:.5s;
}

h2:hover:after {
	width: 9vw;
	background: orange;
    }

@media screen and (max-width: 768px) {
  h2:after {
    width: 15vw;
  }

  h2:hover:after {
	width: 20vw;
  }
}

@media screen and (min-width: 2000px) {
  h2:after {
    width: 3vw;
  }

  h2:hover:after {
	width: 4vw;
  }
}



</style>
