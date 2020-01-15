# aacoding-04
jan15
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<style>
.correct{
  background:green;
}
 
.incorrect{
  background:red;
}
</style>
</head>
<body translate="no">
<script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>
<audio controls id="sad">
<source src="https://math.seattleacademy.org/garyanderson/snd/sad.mp3" type="audio/mpeg">
Your browser does not support the audio tag
</audio>
<h1> Anna's groovy list </h1>
<div>Timer: <span id="theTime">0 </span>Score: <span id="score">0</spiv></div>
<ol>
<ol>
<li>\( 2^3 \) <input data-correct:"8"></li>
<li>\( \sqrt[3]{8} \) <input data-correct:"2"></li>
<li>\(8^{\frac{1}{3}} \) <input data-correct:"2"> </li>
<li>\( (\frac{-125}{27})^\tfrac{-2}{3} \) <input data-correct="9/25" /></li>
<li>\( 12^3 \) <input data-correct="1728" /></li>
<li>\( 14^2 \) <input data-correct="196" /></li>
<li>\(400*9 \) <input data-correct="196" /></li>
</ol>
<script id="rendered-js">
console.clear();
const sad= document.getElementById("sad");
console.log(sad);

setInterval(upTime,1000);

function upTime(){
  let theTime = Number($("#theTime").text());
  theTime = theTime + 1;
  $("#theTime").text(theTime);
}
$("input").change(onChange);

function onChange(evt){
  let correct = $(this).data("correct");
  let response = $(this).val();
  
  if(correct == response){
    $(this).removeClass('incorrect').addClass("correct");
    let theScore = Number($("#score").text());
    theScore = theScore + 1;
    $("#score").text(theScore);
  } else{
    $(this).removeClass('correct').addClass("incorrect");
    let theScore= Number($("#score"))
    if(Math.Random()>.9){
      play.Sad();
    }
  }
}
    </script>
</body>
</html>
