<template>
  <div>
    <h1>about me &nbsp;<i class="fas fa-code"></i></h1>
    <div id="one"><img src="../assets/blue20.png" align="left" width="130px" height="130px">
    <p>recent graduate from university of east anglia. currently working as a front-end developer in london. 
      interested in video game development, full stack development, and cool web design</p>
    <p><b>skills: </b> html, css, javascript (node, react, vue), c#, unity, mysql</p>
    <p>creator of <a href="https://roll-for.herokuapp.com"><u>roll for initiative</u></a>, a react.js app</p>
  </div>
  </div>
</template>

<script>
export default {
  name: "aboutSection",
  props: {

  }
};
</script>

<style>
#one {
  width: 450px;
  text-align: justify;
  left: 0;
  right: 0;
  margin: auto;
}

#one img {
  margin-left: -15px;
  padding-right: 20px;
  border-radius: 50%;
}
</style>