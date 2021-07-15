<template>

  <div id="app">

    <Jumbo mainheading="James Phan" subtext="I am a web developer based in Sydney, Australia. My passion is building simple, beautiful, and functional user experiences. Check out some of my work below."></Jumbo>

    <Heading heading="Projects" id="projects"></Heading>

    <ProjectCard title="Donations XYZ" technologies="HTML5, SCSS, jQuery, Laravel, Bulma" projectduration="May 21" body="A donation form featuring stripe integration, address lookup, donation handles utilising automatic image optimisation, charity selection, and pdf invoice generation." cardback="blur_back xyz_back" button1="btn btn-light btn-sm shadow-sm bg-white rounded" href="https://invoice.jphan.info" buttontext="Live Demo"></ProjectCard>

    <ProjectCard title="Rustled Jimmies" technologies="HTML5, CSS3, JavaScript" projectduration="Dec 20" body="Shhh... no tears. Only dreams now - All is calm, when you let the flow of rustled jimmies take you away. A one hour speedrun project, this page is a homage to one of the greatest sites ever published during the golden era of the internet." cardback="blur_back jimmies_back" button1="btn btn-light btn-sm shadow-sm bg-white rounded" href="https://rustledjimmies.jphan.info" buttontext="Live Demo"></ProjectCard>

    <ProjectCard title="Alpha Omega Consulting" technologies="HTML5, SCSS, Laravel, Bulma" projectduration="Jun 19" body="A responsive website for an NDIS provider that delivers high quality care services across Sydney to seniors and to those living with disabilities." cardback="blur_back aoc_back" button1="btn btn-light btn-sm shadow-sm bg-white rounded" href="https://alphaomegaconsulting.com.au" buttontext="Live Site"></ProjectCard>

    <ProjectCard title="Personal Blog" technologies="HTML5, SCSS, Laravel, Bulma" projectduration="Apr 19" body="A small personal blog to document travels, projects, provide guides and tutorials as well as product reviews, and showcase photos." cardback="blur_back blog_back" button1="btn btn-light btn-sm shadow-sm bg-white rounded" href="https://blog.jphan.info" buttontext="Live Demo"></ProjectCard>

    <ProjectCard title="Tiddoo" technologies="HTML5, SCSS, Vue, Vuex, Laravel, Pusher, Bootstrap" projectduration="Feb 19" body="From work to play, get stuff done easily using Tiddoo. Tiddoo is a simple to-do web application built with VueJS and Laravel, using Pusher to add realtime functionality." cardback="blur_back tiddoo_back" button1="btn btn-light btn-sm shadow-sm bg-white rounded" href="https://tiddoo.jphan.info" buttontext="Live Demo"></ProjectCard>

    <ProjectCard title="Portfolio" technologies="HTML5, CSS3, Vue, Bootstrap" projectduration="Jan 19" body="This page! Have a geez at some of the work I've done. This portfolio was built with VueJS and Bootstrap, an excellent entry point to JavaScript frameworks." cardback="blur_back portfolio_back" button1="btn btn-light btn-sm shadow-sm bg-white rounded" href="https://jphan.info" buttontext="Live Demo"></ProjectCard>

    <ProjectCard title="Minto Family Medical Centre" technologies="HTML5, CSS3, Laravel, Bootstrap" projectduration="Jan 19" body="A revamped version of a local medical centre's website supporting mobile, tablet, and desktop sizes. Includes updated news section and accounts enabling publication of articles regarding general medical or practice related news." cardback="blur_back mfmc_back" button1="btn btn-light btn-sm shadow-sm bg-white rounded" href="https://mintofamilymedicalcentre.com.au" buttontext="Live Site"></ProjectCard>

    <ProjectCard title="ABC Filters" technologies="HTML5, CSS3, jQuery, Laravel, Bootstrap" projectduration="Jul 18 - Dec 18" body="Applied techniques learnt throughout university - from web development to database design to project management. This web application was designed for a local business to automate their invoicing system and provide an updated responsive site design." cardback="blur_back abcfilters_back" button1="btn btn-light btn-sm shadow-sm bg-white rounded d-none" href="https://abcf.jphan.info" buttontext="Screenshots"></ProjectCard>

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
  font-display: swap;
  font-style: normal;
  font-weight: 300;
  src: url('../src/assets/fonts/cormorant-garamond-v6-latin-300.eot'); /* IE9 Compat Modes */
  src: local('Cormorant Garamond Light'), local('CormorantGaramond-Light'),
       url('../src/assets/fonts/cormorant-garamond-v6-latin-300.eot?#iefix') format('embedded-opentype'), /* IE6-IE8 */
       url('../src/assets/fonts/cormorant-garamond-v6-latin-300.woff2') format('woff2'), /* Super Modern Browsers */
       url('../src/assets/fonts/cormorant-garamond-v6-latin-300.woff') format('woff'), /* Modern Browsers */
       url('../src/assets/fonts/cormorant-garamond-v6-latin-300.ttf') format('truetype'), /* Safari, Android, iOS */
       url('../src/assets/fonts/cormorant-garamond-v6-latin-300.svg#CormorantGaramond') format('svg'); /* Legacy iOS */
}

/* montserrat-300 - latin */
@font-face {
  font-family: 'Montserrat';
  font-display: swap;
  font-style: normal;
  font-weight: 300;
  src: url('../src/assets/fonts/montserrat-v12-latin-300.eot'); /* IE9 Compat Modes */
  src: local('Montserrat Light'), local('Montserrat-Light'),
       url('../src/assets/fonts/montserrat-v12-latin-300.eot?#iefix') format('embedded-opentype'), /* IE6-IE8 */
       url('../src/assets/fonts/montserrat-v12-latin-300.woff2') format('woff2'), /* Super Modern Browsers */
       url('../src/assets/fonts/montserrat-v12-latin-300.woff') format('woff'), /* Modern Browsers */
       url('../src/assets/fonts/montserrat-v12-latin-300.ttf') format('truetype'), /* Safari, Android, iOS */
       url('../src/assets/fonts/montserrat-v12-latin-300.svg#Montserrat') format('svg'); /* Legacy iOS */
}
/* montserrat-regular - latin */
@font-face {
  font-family: 'Montserrat';
  font-display: swap;
  font-style: normal;
  font-weight: 400;
  src: url('../src/assets/fonts/montserrat-v12-latin-regular.eot'); /* IE9 Compat Modes */
  src: local('Montserrat Regular'), local('Montserrat-Regular'),
       url('../src/assets/fonts/montserrat-v12-latin-regular.eot?#iefix') format('embedded-opentype'), /* IE6-IE8 */
       url('../src/assets/fonts/montserrat-v12-latin-regular.woff2') format('woff2'), /* Super Modern Browsers */
       url('../src/assets/fonts/montserrat-v12-latin-regular.woff') format('woff'), /* Modern Browsers */
       url('../src/assets/fonts/montserrat-v12-latin-regular.ttf') format('truetype'), /* Safari, Android, iOS */
       url('../src/assets/fonts/montserrat-v12-latin-regular.svg#Montserrat') format('svg'); /* Legacy iOS */
}

html, body {
  font-family: 'Montserrat', helvetica, arial, sans-serif;
}

.no-webp .xyz_back {
  background-image: url("~@/assets/img/xyz.jpg");
}

.webp .xyz_back{
  background-image: url("~@/assets/img/xyz.webp");
}

.no-webp .jimmies_back {
  background-image: url("~@/assets/img/jimmies.jpg");
}

.webp .jimmies_back{
  background-image: url("~@/assets/img/jimmies.webp");
}

.no-webp .aoc_back {
  background-image: url("~@/assets/img/aoc.jpg");
}

.webp .aoc_back{
  background-image: url("~@/assets/img/aoc.webp");
}

.no-webp .blog_back {
  background-image: url("~@/assets/img/blog.jpeg");
}

.webp .blog_back{
  background-image: url("~@/assets/img/blog.webp");
}

.no-webp .tiddoo_back {
  background-image: url("~@/assets/img/tiddoo.jpg");
}

.webp .tiddoo_back{
  background-image: url("~@/assets/img/tiddoo.webp");
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
