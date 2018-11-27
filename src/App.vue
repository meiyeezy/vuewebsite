<template>
  <div id="app">
   <link rel="stylesheet" href="https://use.fontawesome.com/releases/v5.5.0/css/all.css" integrity="sha384-B4dIYHKNBt8Bc12p+WXckhzcICo0wtJAoU8YZTY5qE0Id1GSseTk6S+L3BlXeVIU" crossorigin="anonymous">

    <full-page ref="fullpage" :options="options" id="fullpage">
      <div class="section">
        <HelloWorld />
      </div>
      <div class="section">
        <aboutSection />
      </div>
      <div class="section">
        <contactSection />
      </div>
    </full-page> 
     <ul id="menu">
      <li data-menuanchor="intro" class="active"><a href="#intro">intro</a></li>
      <li data-menuanchor="about"><a href="#about">about</a></li>
      <li data-menuanchor="contact"><a href="#contact">contact</a></li>
    </ul>
    <i class="fas fa-angle-down floating" id="down" @click="$refs.fullpage.api.moveSectionDown()"></i>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import aboutSection from "./components/aboutSection.vue";
import contactSection from "./components/contactSection.vue";

export default {
  name: "app",
  components: {
    HelloWorld,
    aboutSection,
    contactSection
  },
  data: function() {
    return {
      options: {
        licenseKey: "OPEN-SOURCE-GPLV3-LICENSE",
        anchors: ["intro", "about", "contact"],
        menu: "#menu",
        loopBottom: true
      }
    };
  }
};
</script>

<style>
@import url("https://fonts.googleapis.com/css?family=Karla|Montserrat");

body, html {
  margin: 0; 
  padding: 0;
  width: 100%; 
  height: 100%;
}

#down {
  position: absolute;
  width: 0;
  bottom: 15px;
  font-size: 25px;
  left: 0;
  right: 0;
  margin: auto;
  cursor: pointer;
}

#app {
  font-family: "Montserrat", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}

p {
  font-size: 12px;
}

h1 {
  font-family: "Karla";
}

#menu {
  position: absolute;
  right: 10px;
  top: 5px;
}

#menu li {
  display: inline-block;
  padding-right: 20px;
  font-weight: bold;
}

li { 
  list-style-type: none;
}

a {
  text-decoration: none;
  color: #2c3e50;
}

a:visited {
  color: #2c3e50;
}

.section {
  margin-top: -50px;
}

.fp-tableCell {
  display: table-cell;
  vertical-align: middle;
  text-align: center;
  width: 100vw;
  height: 100vh;
}

.floating{
	animation-name: floating;
	-webkit-animation-name: floating;
	animation-duration: 1.5s;
	-webkit-animation-duration: 1.5s;
	animation-iteration-count: infinite;
	-webkit-animation-iteration-count: infinite;
}
@keyframes floating {
	0% {
		transform: translateY(0%);
	}
	50% {
		transform: translateY(10%);
	}
	100% {
		transform: translateY(0%);
	}
}
</style>
