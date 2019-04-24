<template>
  <div>
    <h1>about me &nbsp;<i class="fas fa-code"></i></h1>
    <div id="one"><img src="../assets/pic2.jpg" align="left" width="130px" height="130px">
    <p>computer science graduate from university of east anglia. currently working as a junior games designer in central london. 
      interested in gaming, dungeons and dragons, video game development, full stack development, and funky web design</p>
    <p><b>skills: </b> html, css, javascript (node, react, vue), c#, unity, mysql, basic oop (c, c++, java)</p>
    <p><b>creator and owner of: </b> <a href="https://roll-for.herokuapp.com" target="_blank"><u>roll for initiative</u></a>, a react.js app; 
    <a href="https://twitter.com/critcosplaybot" target="_blank"><u>critical role cosplay bot</u></a>, a node.js twitter bot</p>
    <p><b>working on: </b> learning unity3d, making my own games</p>
  </div>
  </div>
</template>

<script>
export default {
  name: "aboutSection"
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
  margin-right: 20px;
  border-radius: 50%;
}
</style>