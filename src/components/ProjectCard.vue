<template>

<div class="project_card">

  <div class="info_section">

    <div class="project_header">

      <h1> {{ title }} </h1>

      <h6> {{ projectduration }} </h6>

      <p class="technologies"> {{ technologies }} </p>

    </div>

    <div class="description">

      <p class="text">

        {{ body }}

      </p>

    </div>

    <div class="links">

      <ul>

        <li><a :class="button1" :href="href"><slot></slot> {{ buttontext }} </a></li>

      </ul>

    </div>

  </div>

  <div :class="cardback"><slot></slot></div>

</div>

</template>



<script>

export default {

  props: ["title", "body", "technologies", "projectduration", "background", "cardback", "href", "buttontext", "button1"],

}

</script>



<style>

* {
  box-sizing: border-box;
  margin: 0;
}

html, body {
  margin: 0;
  background: white;
  font-size: 14px;
  font-weight: 400;
}

.link {
  display: block;
  text-align: center;
  color: #777;
  text-decoration: none;
  padding: 10px;
}

.project_card {
  position: relative;
  display: block;
  width: 800px;
  height: 350px;
  margin: 80px auto;
  overflow: hidden;
  border-radius: 4px;
  transition: all 0.4s;
  box-shadow: 0px 0px 120px -25px rgba(0, 0, 0, 0.5);
}
.project_card:hover {
  -webkit-transform: scale(1.02);
          transform: scale(1.02);
  box-shadow: 0px 0px 80px -25px rgba(0, 0, 0, 0.5);
  transition: all 0.4s;
}
.project_card .info_section {
  position: relative;
  width: 100%;
  height: 100%;
  background-blend-mode: multiply;
  z-index: 2;
  border-radius: 4px;
}
.project_card .info_section .project_header {
  position: relative;
  padding: 25px;
  height: 40%;
}
.project_card .info_section .project_header h1 {
  color: black;
  font-weight: 400;
}
.project_card .info_section .project_header h4 {
  color: #555;
  font-weight: 400;
}

.project_card .info_section .project_header .technologies {
  display: inline-block;
  color: #959595;
}

.project_card .info_section .description {
  padding: 25px;
  height: 47%;
}
.project_card .info_section .description .text {
  color: #545454;
  padding-bottom: 50px
}
.project_card .info_section .links {
  height: 10%;
  padding-left: 15px;
  padding-bottom: 20px;
}
.project_card .info_section .links ul {
  list-style: none;
  padding: 0;
}
.project_card .info_section .links ul li {
  display: inline-block;
  color: rgba(0, 0, 0, 0.3);
  transition: color 0.3s;
  transition-delay: 0.15s;
  margin: 0 10px;
}
.project_card .info_section .links ul li:hover {
  transition: color 0.3s;
  color: rgba(0, 0, 0, 0.7);
}
.project_card .info_section .links ul li i {
  font-size: 19px;
  cursor: pointer;
}
.project_card .blur_back {
  position: absolute;
  top: 0;
  z-index: 1;
  height: 100%;
  right: 0;
  background-size: cover;
  border-radius: 5px;
}

@media screen and (min-width: 768px) {
  .project_header {
    width: 60%;
  }

  .description {
    width: 50%;
  }

  .info_section {
    background: linear-gradient(to right, #e5e6e6 50%, transparent 100%);
  }

  .blur_back {
    width: 80%;
    background-position: -100% 10% !important;
  }
}
@media screen and (max-width: 768px) {
  .project_card {
    width: 85%;
    margin: 70px auto;
    /*min-height: 350px;
*/    height: auto;
  }

  .blur_back {
    width: 100%;
    background-position: 50% 50% !important;
  }

  .project_header {
    width: 100%;
    margin-top: 20px;
    text-shadow: 0 0 8px white;
  }

  .project_card .info_section .project_header .technologies {
    color: #505050;
  }

  .description {
    width: 100%;
  }

  .info_section {
    background: linear-gradient(to top, #e5e6e6 50%, transparent 100%);
    display: inline-grid;
  }
  .text {
    margin-top: 50px;
    padding-bottom: 0px !important;
  }
}

</style>
