<template>

    <footer>
      
      <div class="container">

        <p class="text-center text-muteed">{{ footer }} &copy; {{ new Date().getFullYear() }}</p>

      </div>

    </footer>

</template>



<script>

export default {

  props: ["footer"],

}

</script>

<style scoped>

p {
	font-size: 0.9em;
	color: #5a5d7a;
	padding-bottom: 50px;
}


</style>
