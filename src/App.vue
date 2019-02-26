<template>

  <div id="app">

    <Jumbo mainheading="James Phan" subtext="I am a full stack web developer based in Sydney, Australia. My passion is building simple, beautiful, and functional user experiences. Check out some of my work below."></Jumbo>

    <Heading heading="Projects" id="projects"></Heading>

    <ProjectCard title="Portfolio" technologies="HTML5, CSS3, Vue, Bootstrap" projectduration="Feb 19" body="This page! This portfolio was built using VueJS and was an excellent entry point to JavaScript frameworks." classy="blur_back portfolio_back" href="http://jphan.info" buttontext="Live Demo"></ProjectCard>

    <ProjectCard title="Minto Family Medical Centre" technologies="HTML5, CSS3, Laravel, Bootstrap" projectduration="Dec 18 - Jan 19" body="A revamped version of a local medical centre's website supporting mobile, tablet, and desktop sizes. Includes updated news section and accounts enabling publication of articles regarding general medical or practice related news." classy="blur_back mfmc_back" href="http://mfmc.jphan.info" buttontext="Live Demo"></ProjectCard>

    <ProjectCard title="ABC Filters" technologies="HTML5, CSS3, JS, Laravel" projectduration="Jul 18 - Dec 18" body="Applied techniques learnt throughout university - from web development to database design to project management. This web application was designed for a local business to automate their invoicing system and provide an updated responsive site design." classy="blur_back abcfilters_back" buttontext="Screenshots"></ProjectCard>

    <Heading heading="Contact" id="contact"></Heading>

    <ContactLinks></ContactLinks>

    <Footer footer="Made by James Phan"></Footer>

  </div>

</template>



<script>

import ProjectCard from './components/ProjectCard.vue'

import Jumbo from './components/Jumbo.vue'

import Heading from './components/Heading.vue'

import ContactLinks from './components/ContactLinks.vue'

import Footer from './components/Footer.vue'

export default {

  name: 'app',

  components: { ProjectCard, Jumbo, Heading, ContactLinks, Footer },

  data() {

    return {

    }

  }

}

</script>



<style>

/* cormorant-garamond-300 - latin */
@font-face {
  font-family: 'Cormorant Garamond';
  font-style: normal;
  font-weight: 300;
  src: url('../src/assets/fonts/cormorant-garamond-v6-latin-300.eot'); /* IE9 Compat Modes */
  src: local('Cormorant Garamond Light'), local('CormorantGaramond-Light'),
       url('../src/assets/fonts/cormorant-garamond-v6-latin-300.eot?#iefix') format('embedded-opentype'), /* IE6-IE8 */
       url('../src/assets/fonts/cormorant-garamond-v6-latin-300.woff2') format('woff2'), /* Super Modern Browsers */
       url('../src/assets/fonts/cormorant-garamond-v6-latin-300.woff') format('woff'), /* Modern Browsers */
       url('../src/assets/fonts/cormorant-garamond-v6-latin-300.ttf') format('truetype'), /* Safari, Android, iOS */
       url('../src/assets/fonts/cormorant-garamond-v6-latin-300.svg#CormorantGaramond') format('svg'); /* Legacy iOS */
  font-display: 'swap';
}

/* montserrat-300 - latin */
@font-face {
  font-family: 'Montserrat';
  font-style: normal;
  font-weight: 300;
  src: url('../src/assets/fonts/montserrat-v12-latin-300.eot'); /* IE9 Compat Modes */
  src: local('Montserrat Light'), local('Montserrat-Light'),
       url('../src/assets/fonts/montserrat-v12-latin-300.eot?#iefix') format('embedded-opentype'), /* IE6-IE8 */
       url('../src/assets/fonts/montserrat-v12-latin-300.woff2') format('woff2'), /* Super Modern Browsers */
       url('../src/assets/fonts/montserrat-v12-latin-300.woff') format('woff'), /* Modern Browsers */
       url('../src/assets/fonts/montserrat-v12-latin-300.ttf') format('truetype'), /* Safari, Android, iOS */
       url('../src/assets/fonts/montserrat-v12-latin-300.svg#Montserrat') format('svg'); /* Legacy iOS */
  font-display: 'swap';
}
/* montserrat-regular - latin */
@font-face {
  font-family: 'Montserrat';
  font-style: normal;
  font-weight: 400;
  src: url('../src/assets/fonts/montserrat-v12-latin-regular.eot'); /* IE9 Compat Modes */
  src: local('Montserrat Regular'), local('Montserrat-Regular'),
       url('../src/assets/fonts/montserrat-v12-latin-regular.eot?#iefix') format('embedded-opentype'), /* IE6-IE8 */
       url('../src/assets/fonts/montserrat-v12-latin-regular.woff2') format('woff2'), /* Super Modern Browsers */
       url('../src/assets/fonts/montserrat-v12-latin-regular.woff') format('woff'), /* Modern Browsers */
       url('../src/assets/fonts/montserrat-v12-latin-regular.ttf') format('truetype'), /* Safari, Android, iOS */
       url('../src/assets/fonts/montserrat-v12-latin-regular.svg#Montserrat') format('svg'); /* Legacy iOS */
  font-display: 'swap';
}

html, body {
  font-family: 'Montserrat', helvetica, arial, sans-serif;
}

.no-webp .portfolio_back {
  background-image: url("~@/assets/img/portfolio.jpg");
}

.webp .portfolio_back{
  background-image: url("~@/assets/img/portfolio.webp");
}

.no-webp .mfmc_back {
  background-image: url("~@/assets/img/mfmc.jpg");
}

.webp .mfmc_back{
  background-image: url("~@/assets/img/mfmc.webp");
}

.no-webp .abcfilters_back {
  background-image: url("~@/assets/img/abcfilters.png");
}

.webp .abcfilters_back{
  background-image: url("~@/assets/img/abcfilters.webp");
}

</style>
