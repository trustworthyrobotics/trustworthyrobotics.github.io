---
layout: page
---

<img align="center" id="responsive-image" src="images/lab_icon_v2.png" style="width: 100%; max-width: 1500px; margin:  0 auto; transition: margin-top 0.3s ease;">

<!-- <div style="display: flex; align-items: center; justify-content: center; gap: 0px;">
    <div style="flex: 1;">
        <span style="font-weight:bold">Assistant Professor</span><br>
        <span style="font-weight:bold">Georgia Institute of Technology</span><br>
        <span style="font-weight:bold">Office</span>: CODA <br>
        <span style="font-weight:bold">Email: </span>chou [at] gatech [dot] edu<br>
        <span style="font-weight:bold"> <a href="cv_08_19_24.pdf"> CV</a>&nbsp;&nbsp;|&nbsp;  </span>
        <span style="font-weight:bold"><i class="ai ai-google-scholar-square ai-1x"></i> <a href="https://scholar.google.com/citations?user=90whi3wAAAAJ&hl">Scholar</a>&nbsp;&nbsp;|&nbsp;  </span>
        <span style="font-weight:bold"><i class="ai ai-researchgate-square ai-1x"></i> <a href="https://www.researchgate.net/profile/Glen_Chou"> ResearchGate</a>  </span>
    </div>
    <div style="flex: 1;">
        <img align="right" id="responsive-image" src="images/glen.png" style="margin: -80px 0px 10px 10px; width: 235px; border-radius:50%; transition: margin-top 0.3s ease;">
    </div>
</div> -->

<div style="width: 90%; max-width: 1200px; overflow: hidden; border: 1px solid #ccc; padding: 10px; margin:  0 auto;">
  <div id="content" style="max-height: 60px; overflow: hidden; transition: max-height 0.5s ease;">
    <p><span style="color:  red;"><b><i>News:</i></b></span> We are actively recruiting PhD students to join the lab in Fall 2025, and we are also looking for driven UG and MS Georgia Tech students to contribute to our research. See the <a href="openings/">openings</a> page for more details.</p>
  </div>
  <button id="moreButton" onclick="revealMore()" style="margin-top: 10px;">More</button>
</div>
<br>


<!-- ## Research focus: -->
<p> Welcome! The Trustworthy Robotics Lab at Georgia Tech, directed by <a href="https://glenchou.github.io/"> Glen Chou</a>, designs principled algorithms that can enable general-purpose robots and autonomous systems to operate capably, safely, and securely with humans, while remaining resilient to real-world failures and uncertainty.</p> <p>To achieve this, we leverage control and machine learning, while connecting to optimization, perception, formal methods, planning, human-robot interaction, and statistics. We're interested in broad applications of autonomy, including robotic manipulation, vision-based navigation, aerospace, and large-scale cyber-physical systems more generally. Check out the links below or <a href="projects/">this page</a> for an overview of our work. </p>

<!-- <h2 id="research-overview">Research overview:</h2>
<div style="width: 100%; text-align: center;">
<iframe width="528" height="297"
src="https://www.youtube.com/embed/MUQfKFzIOeU" 
frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>
</div> -->

<style>
    table.areas {
        display: table;
        text-align: center;
        margin: 0 auto;
    }
    table.areas tr {
        display: table-cell;
        width: 33%;
        border-radius: 5px;
        box-shadow: 0 0 25px 5px rgba(0,0,0,0.12);
    }
    table.areas tr:hover {
        background-color: rgba(0,117,97,0.2);
        cursor: pointer;
    }
    table.areas tr td {
        display: block;
    }
    table.areas tr td.ar_img {
        display: flex;
        align-items: center;
        justify-content: center;
        height: 17em;
    }
    table.areas tr td.ar_img img {
        height:100%;
        object-fit: cover;
        padding-bottom: 0;
    }
    table.areas tr td.ar_text {
        display: block;
        height: 5em;
        vertical-align: top;
        padding-top: 0;
        padding-bottom: 1vh;
        line-height: 1;
    }
    @media screen and (max-width: 1024px) {
        table.areas tr {
            display: block;
            width: 100%; /* Set the width to 100% for smaller screens */
            box-sizing: border-box;
            margin-bottom: 10px; /* Adjust as needed */
        }
    }
</style>

<table class="areas">
        <tr onclick="window.location='projects/verified_control'">
                <td class="ar_img"><img src="/images/isls.gif"/></td>
                <td class="ar_text"><h2 style="font-size:1.5em"><a>Formally-Verified Model-Based <br> Control Synthesis</a></h2></td>
        </tr>
        <tr onclick="window.location='projects/learning_based_control'">
                <td class="ar_img"><img src="/images/icra_23b_alt.gif" /></td>
                <td class="ar_text"><h2 style="font-size:1.5em"><a>Trustworthy Learning-Based <br> Planning and Control <br></a></h2></td>
        </tr>
        <tr onclick="window.location='projects/safe_lfd'">
                <td class="ar_img"><img src="/images/auro_22_02.gif" /></td>
                <td class="ar_text"><h2 style="font-size:1.5em"><a>Safe and Robust <br> Human-Robot Interaction</a></h2></td>
        </tr>
</table>

<script>
  function revealMore() {
    var content = document.getElementById("content");
    var button = document.getElementById("moreButton");
    var currentHeight = content.clientHeight;
    var lineHeight = 20; // Adjust based on your content's line height
    var newHeight = currentHeight + lineHeight * 10; // Reveal 3 more lines

    if (newHeight < content.scrollHeight) {
      content.style.maxHeight = newHeight + "px";
    } else {
      content.style.maxHeight = content.scrollHeight + "px";
      button.style.display = "none"; // Hide the button when all content is revealed
    }
  }
</script>
