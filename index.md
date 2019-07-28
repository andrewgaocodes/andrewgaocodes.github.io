<html>
<title>W3.CSS</title>
<meta name="viewport" content="width=device-width, initial-scale=1">
<link rel="stylesheet" href="https://www.w3schools.com/w3css/4/w3.css">
<style>
  img.resize {
  max-width:50%;
  max-height:50%;
    border-radius: 8px;

}
  </style>
<body>

<div class="w3-container">
  <div class="w3-row">
    <a href="javascript:void(0)" onclick="openSection(event, 'About Me');">
      <div class="w3-third tablink w3-bottombar w3-hover-light-grey w3-padding" style="text-align:center">About Me</div>
    </a>
    <a href="javascript:void(0)" onclick="openSection(event, 'My Projects');">
      <div class="w3-third tablink w3-bottombar w3-hover-light-grey w3-padding" style="text-align:center">My Projects</div>
    </a>
    <a href="javascript:void(0)" onclick="openSection(event, 'My Experience');">
      <div class="w3-third tablink w3-bottombar w3-hover-light-grey w3-padding" style="text-align:center">My Experience</div>
    </a>
  </div>

  <div id="About Me" class="w3-container city" style="display:none">
    <h2>About Me</h2>
  <img id="portrait"  class = "resize" src="IMG_1628.jpg" alt="Photo of Andrew Gao">

  <p>Hi! I'm Andy, from San Diego, CA. I'm passionate about programming, biology, entrepreneurship and more. In my free time, I like to read about cultural anthropology. Currently I'm organizing <a href="ravenhack.org">Raven Hack</a>, San Diego's <strong>first</strong> free hackathon for all high schoolers.</p>
  </div>

  <div id="My Projects" class="w3-container city" style="display:none">
    <h2>My Projects</h2>
    <p>My Projects</p> 
  </div>

  <div id="My Experience" class="w3-container city" style="display:none">
    <h2>My Experience</h2>
    <p>My Experience</p>
  </div>
</div>

<script>
function openSection(evt, cityName) {
  var i, x, tablinks;
  x = document.getElementsByClassName("city");
  for (i = 0; i < x.length; i++) {
    x[i].style.display = "none";
  }
  tablinks = document.getElementsByClassName("tablink");
  for (i = 0; i < x.length; i++) {
    tablinks[i].className = tablinks[i].className.replace(" w3-border-blue", "");
  }
  document.getElementById(cityName).style.display = "block";
  evt.currentTarget.firstElementChild.className += " w3-border-blue";
}
</script>

</body>
</html>
