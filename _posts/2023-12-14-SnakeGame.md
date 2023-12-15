---
toc: false
comments: false
layout: post
title: Classic Snake Game
description: A pretty advanced use of JavaScript building classic snake game using menu controls, key events, snake simulation and timers.
type: tangibles
courses: { compsci: {week: 5} }
---

<main>
<div id="game-modes-wrapper">
    <div id="mode-1" class="mode">
        <h3>Border Mode</h3>
        <button id="start-game-1" class="btn">Start</button>
    </div>
    
<div id="mode-2" class="mode">
    <h3>Borderless Mode</h3>
    <button id="start-game-2" class="btn">Start</button>
</div>

<div id="mode-3" class="mode">
    <h3>Peaceful Mode</h3>
    <button id="start-game-3" class="btn">Start</button>
</div>

<div id="mode-4" class="mode">
    <h3>Winged Mode</h3>
    <button id="start-game-4" class="btn">Start</button>
</div>

<div id="mode-5" class="mode">
    <h3>Cheese Mode</h3>
    <button id="start-game-5" class="btn">Start</button>
</div>

<div id="mode-6" class="mode">
    <h3>Timer Mode</h3>
    <button id="start-game-6" class="btn">Start</button>
</div>

<div id="mode-7" class="mode">
    <h3>Dual Mode</h3>
    <button id="start-game-7" class="btn">Start</button>
</div>

<div id="mode-8" class="mode">
    <h3>Double-headed Mode</h3>
    <button id="start-game-8" class="btn">Start</button>
</div>

<div id="mode-9" class="mode">
    <h3>Portal Mode</h3>
    <button id="start-game-9" class="btn">Start</button>
</div>
</div>


<div id="game-wrapper">
    <div id="score-wrapper">
        <div><span>Score: </span><span id="total-score">0</span></div>
        <div><span>Length: </span><span id="length-score">4</span></div>
        <div><span>Fruits: </span><span id="food-score">0</span></div>
    </div>
    <canvas width="300" height="400"></canvas>
</div>
</main>



<script src="{{site.baseurl}}/assets/js/utils/snake.js"></script>
<script src="{{site.baseurl}}/assets/js/utils/snakeCheesy.js"></script>
<script src="{{site.baseurl}}/assets/js/utils/food.js"></script>
<script src="{{site.baseurl}}/assets/js/utils/foodWinged.js"></script>
<script src="{{site.baseurl}}/assets/js/utils/score.js"></script>
<script src="{{site.baseurl}}/assets/js/utils/gameCanvas.js"></script>
<script src="{{site.baseurl}}/assets/js/utils/sounds.js"></script>

<script src="{{site.baseurl}}/assets/js/game/mainGame1.js"></script>
<script src="{{site.baseurl}}/assets/js/game/mainGame2.js"></script>
<script src="{{site.baseurl}}/assets/js/game/mainGame3.js"></script>
<script src="{{site.baseurl}}/assets/js/game/mainGame4.js"></script>
<script src="{{site.baseurl}}/assets/js/game/mainGame5.js"></script>
<script src="{{site.baseurl}}/assets/js/game/mainGame6.js"></script>
<script src="{{site.baseurl}}/assets/js/game/mainGame7.js"></script>
<script src="{{site.baseurl}}/assets/js/game/mainGame8.js"></script>
<script src="{{site.baseurl}}/assets/js/game/mainGame9.js"></script>

<script src="{{site.baseurl}}/assets/js/init/gameInit.js"></script>
<script src="{{site.baseurl}}/assets/js/init/loader.js"></script>

<style>
    
@import url('https://fonts.googleapis.com/css2?family=Nunito&family=PT+Sans&family=Roboto:wght@400;700&display=swap');

:root
{
	--theme: #BCD5EA;
	--theme-light: #c4eebb;
}

*
{
	padding: 0;
	margin: 0;
	box-sizing: border-box;
	font-family: 'Nunito', sans-serif;
}

body
{
	background: url("{{site.baseurl}}/images/bg.png");
}


header
{
	display: flex;
	padding: 20px;
	background-color: var(--theme);
	color: white;
}

header #home
{
	flex-grow: 0;
	display: inline-block;
	font-size: 20px;
	cursor: pointer;
	color: white;
	text-decoration: none;
	border-radius: 3px;
	line-height: 40px;
	font-weight: bold;
	transition: 0.5s;
}

header #home:hover
{
	color: #BCD5EA;
}

header h1
{
	flex-grow: 1;
	text-align: center;
}


.btn
{
	background-color: #CEE2F2;
	font-size: 20px;
	color: var(--theme);
	border: 2px solid var(--theme);
	padding: 10px;
	border-radius: 3px;
	cursor: pointer;
	transition: 0.5s;
	width: 100px;
	margin: 10px;
	font-weight: bold;
}

.btn:hover
{
	box-shadow: 2px 2px 3px grey;
	background-color: var(--theme);
	color: white;
}

#game-modes-wrapper
{
	display: flex;
	flex-wrap: wrap;
	justify-content: center;
	padding-top: 20px;
}

.mode
{
	padding: 20px;
	margin: 10px;
	width: 300px;
	height: 150px;
	text-align: center;
	background-color: white;
	box-shadow: 2px 2px 4px gray;
}

.mode .btn
{
	margin: 15px;
}




#game-wrapper
{
	display: none;
	padding-top: 15px;
}

#score-wrapper
{
	margin: 20px 0%;
	font-size: 20px;
	display: flex;
}

#score-wrapper > div
{
	/* flex-grow: 1; */
	width: 33%;
	text-align: center;
}

#timer
{
	color: red;
	font-weight: bold;
	margin-left: 20px;
	font-size: 20px;
	background-color: white;
	width: fit-content;
	padding: 5px;
	border-radius: 3px;
}

canvas
{
	display: block;
	margin: auto;
	border: 5px solid var(--theme);
	background: url("{{site.baseurl}}/images/board.png");
}
    </style>