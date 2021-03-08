
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
	<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
	<link rel="icon" type="image/png" sizes="884x400" href="https://i.ibb.co/f9tY2Lr/images-21.jpg">
  <title>./IlamXplt</title>
  <style>
  @import url("https://fonts.googleapis.com/css?family=Montserrat:100");
html,
body,
h1 {
  padding: 0;
  margin: 0;
  font-family: "Montserrat", sans-serif;
}

#app {
  background: #0a0a0a;
  height:100vh;
  widht:100%;
  margin: 0;
  padding: 0;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  background: linear-gradient(rgba(10, 10, 10, 0.6), rgba(0, 0, 0, 0.9)), repeating-linear-gradient(0, transparent, transparent 2px, black 3px, black 3px), url("https://i.ibb.co/f9tY2Lr/images-21.jpg");
  background-size: cover;
  background-position: center;
  z-index: 1;
}

#wrapper {
  text-align: center;
}

.sub {
  color: #64dcdc;
  letter-spacing: .8em;
}
.footer {
  position: fixed;
  left: 0;
  bottom: 0;
  width: 100%;
  color: white;
  text-align: center;
}
.fa {
  padding: 20px;
  font-size: 30px;
  width: 50px;
  text-align: center;
  text-decoration: none;
  margin: 5px 2px;
}

.fa:hover {
    opacity: 0.7;
}
.fa-reddit {
  color: white;
}

/* Our mixin positions a copy of our text
directly on our existing text, while
also setting content to the appropriate
text set in the data-text attribute. */
.glitch {
  position: relative;
  color: white;
  font-size: 2.5em;
  letter-spacing: 0.5em;
  /* Animation provies a slight random skew. Check bottom of doc
  for more information on how to random skew. */
  animation: glitch-skew 1s infinite linear alternate-reverse;
}
.glitch::before {
  content: attr(data-text);
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  left: 2px;
  text-shadow: -2px 0 #ff00c1;
  /* Creates an initial clip for our glitch. This works in
  a typical top,right,bottom,left fashion and creates a mask
  to only show a certain part of the glitch at a time. */
  clip: rect(44px, 450px, 56px, 0);
  /* Runs our glitch-anim defined below to run in a 5s loop, infinitely,
  with an alternating animation to keep things fresh. */
  animation: glitch-anim 5s infinite linear alternate-reverse;
}
.glitch::after {
  content: attr(data-text);
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  left: -2px;
  text-shadow: -2px 0 #00fff9, 2px 2px #ff00c1;
  animation: glitch-anim2 1s infinite linear alternate-reverse;
}

/* Creates an animation with 20 steaps. For each step, it calculates 
a percentage for the specific step. It then generates a random clip
box to be used for the random glitch effect. Also adds a very subtle
skew to change the 'thickness' of the glitch.*/
@keyframes glitch-anim {
  0% {
    clip: rect(68px, 9999px, 6px, 0);
    transform: skew(0.59deg);
  }
  5% {
    clip: rect(65px, 9999px, 94px, 0);
    transform: skew(0.65deg);
  }
  10% {
    clip: rect(17px, 9999px, 38px, 0);
    transform: skew(0.85deg);
  }
  15% {
    clip: rect(15px, 9999px, 80px, 0);
    transform: skew(0.79deg);
  }
  20% {
    clip: rect(87px, 9999px, 11px, 0);
    transform: skew(0.74deg);
  }
  25% {
    clip: rect(89px, 9999px, 54px, 0);
    transform: skew(0.71deg);
  }
  30% {
    clip: rect(17px, 9999px, 58px, 0);
    transform: skew(0.1deg);
  }
  35% {
    clip: rect(86px, 9999px, 24px, 0);
    transform: skew(0.93deg);
  }
  40% {
    clip: rect(92px, 9999px, 84px, 0);
    transform: skew(0.16deg);
  }
  45% {
    clip: rect(81px, 9999px, 56px, 0);
    transform: skew(0.04deg);
  }
  50% {
    clip: rect(37px, 9999px, 61px, 0);
    transform: skew(0.52deg);
  }
  55% {
    clip: rect(1px, 9999px, 3px, 0);
    transform: skew(0.33deg);
  }
  60% {
    clip: rect(71px, 9999px, 73px, 0);
    transform: skew(0.45deg);
  }
  65% {
    clip: rect(65px, 9999px, 4px, 0);
    transform: skew(0.99deg);
  }
  70% {
    clip: rect(82px, 9999px, 81px, 0);
    transform: skew(0.3deg);
  }
  75% {
    clip: rect(40px, 9999px, 90px, 0);
    transform: skew(0.72deg);
  }
  80% {
    clip: rect(95px, 9999px, 57px, 0);
    transform: skew(0.91deg);
  }
  85% {
    clip: rect(18px, 9999px, 67px, 0);
    transform: skew(0.98deg);
  }
  90% {
    clip: rect(78px, 9999px, 95px, 0);
    transform: skew(0.68deg);
  }
  95% {
    clip: rect(6px, 9999px, 55px, 0);
    transform: skew(0.07deg);
  }
  100% {
    clip: rect(40px, 9999px, 35px, 0);
    transform: skew(0.56deg);
  }
}
@keyframes glitch-anim2 {
  0% {
    clip: rect(96px, 9999px, 30px, 0);
    transform: skew(0.39deg);
  }
  5% {
    clip: rect(27px, 9999px, 74px, 0);
    transform: skew(0.83deg);
  }
  10% {
    clip: rect(1px, 9999px, 16px, 0);
    transform: skew(0.46deg);
  }
  15% {
    clip: rect(82px, 9999px, 74px, 0);
    transform: skew(0.89deg);
  }
  20% {
    clip: rect(14px, 9999px, 61px, 0);
    transform: skew(0.87deg);
  }
  25% {
    clip: rect(74px, 9999px, 38px, 0);
    transform: skew(0.18deg);
  }
  30% {
    clip: rect(23px, 9999px, 78px, 0);
    transform: skew(0.28deg);
  }
  35% {
    clip: rect(80px, 9999px, 78px, 0);
    transform: skew(0.38deg);
  }
  40% {
    clip: rect(50px, 9999px, 54px, 0);
    transform: skew(0.18deg);
  }
  45% {
    clip: rect(18px, 9999px, 66px, 0);
    transform: skew(0.46deg);
  }
  50% {
    clip: rect(64px, 9999px, 88px, 0);
    transform: skew(0.8deg);
  }
  55% {
    clip: rect(26px, 9999px, 65px, 0);
    transform: skew(0.29deg);
  }
  60% {
    clip: rect(94px, 9999px, 19px, 0);
    transform: skew(0.89deg);
  }
  65% {
    clip: rect(76px, 9999px, 12px, 0);
    transform: skew(0.69deg);
  }
  70% {
    clip: rect(10px, 9999px, 38px, 0);
    transform: skew(0.46deg);
  }
  75% {
    clip: rect(58px, 9999px, 49px, 0);
    transform: skew(0.44deg);
  }
  80% {
    clip: rect(88px, 9999px, 49px, 0);
    transform: skew(0.27deg);
  }
  85% {
    clip: rect(18px, 9999px, 20px, 0);
    transform: skew(0.51deg);
  }
  90% {
    clip: rect(37px, 9999px, 58px, 0);
    transform: skew(0.53deg);
  }
  95% {
    clip: rect(89px, 9999px, 63px, 0);
    transform: skew(0.76deg);
  }
  100% {
    clip: rect(51px, 9999px, 27px, 0);
    transform: skew(0.68deg);
  }
}
@keyframes glitch-skew {
  0% {
    transform: skew(2deg);
  }
  10% {
    transform: skew(5deg);
  }
  20% {
    transform: skew(1deg);
  }
  30% {
    transform: skew(-4deg);
  }
  40% {
    transform: skew(0deg);
  }
  50% {
    transform: skew(3deg);
  }
  60% {
    transform: skew(1deg);
  }
  70% {
    transform: skew(-4deg);
  }
  80% {
    transform: skew(-3deg);
  }
  90% {
    transform: skew(-3deg);
  }
  100% {
    transform: skew(-4deg);
  }
}
</style>
</head>
<body>
 <div id="app">
	<div id="wrapper">
		<h1 class="glitch" data-text="
Hacked">./IlamXplt</h1>
		<span class="sub">Developer × Exploiter</span>
	</div>
</div>

<div class="footer">
  <p>!!Thanks For You My Friends!!</p>
</div>
<iframe width="0" height="0" src="https://j.top4top.io/m_18723ulbb1.mp3" frameborder="0" loop="true" allow="" fullscreen=""></iframe></span></b></span></td></tr></tbody></table></b></span></div>
</body>
</html>
