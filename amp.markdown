---
layout: default
title: "主页"
---

### 《布袋豆腐歌》

<!-- Amplitude Player -->
  <div id="amplitude-player">
    <div id="amplitude-left">
      <img data-amplitude-song-info="cover_art_url" class="album-art"/>
      <div class="amplitude-visualization" id="large-visualization"></div>
      <div id="player-left-bottom">
        <div id="time-container">
          <span class="current-time">
            <span class="amplitude-current-minutes" ></span>:<span class="amplitude-current-seconds"></span>
          </span>
          <div id="progress-container">
            <div class="amplitude-wave-form"></div>
            <input type="range" class="amplitude-song-slider"/>
            <progress id="song-played-progress" class="amplitude-song-played-progress"></progress>
            <progress id="song-buffered-progress" class="amplitude-buffered-progress" value="0"></progress>
          </div>
          <span class="duration">
            <span class="amplitude-duration-minutes"></span>:<span class="amplitude-duration-seconds"></span>
          </span>
        </div>
        <div id="control-container">
          <div id="repeat-container">
            <div class="amplitude-repeat" id="repeat"></div>
            <div class="amplitude-shuffle amplitude-shuffle-off" id="shuffle"></div>
          </div>
          <div id="central-control-container">
            <div id="central-controls">
              <div class="amplitude-prev" id="previous"></div>
              <div class="amplitude-play-pause" id="play-pause"></div>
              <div class="amplitude-next" id="next"></div>
            </div>
          </div>
          <div id="volume-container">
            <div class="volume-controls">
              <div class="amplitude-mute amplitude-not-muted"></div>
              <input type="range" class="amplitude-volume-slider"/>
              <div class="ms-range-fix"></div>
            </div>
            <div class="amplitude-shuffle amplitude-shuffle-off" id="shuffle-right"></div>
          </div>
        </div>
        <div id="meta-container">
          <span data-amplitude-song-info="name" class="song-name"></span>
          <div class="song-artist-album">
            <span data-amplitude-song-info="artist"></span>
            <span data-amplitude-song-info="album"></span>
          </div>
        </div>
      </div>
    </div>
</div>


用老工艺，无高科技；不为增产，加添加剂；<br>
布袋豆腐，按照规矩，老老实实，不随恶欲。

好不骄慢，不非实赞；恶不覆藏，直示人知。<br>
卖不轻称，端心不欺；应行多行，常念布施。

虽谋世利，不无厌行。念他如己，财不如意；<br>
不悕厚利，忍知足行。亦不贪心，窃他财行。

虽自有苦，当正观行；过去痴心，作诸恶行，<br>
是苦因生，如是受行；不应纵痴，复苦业行。

念圣忍行，忍如地行；念苦因行，不放逸行，<br>
勿懈退行，苦尽道行；观法性行，唯空寂性。

正念慧剑，常斩恶行；生惭愧行，是为善行；<br>
悟过恶行，慎行不行；调身意行，归大乘行。

虽世业行，不世乐行；念所善行，为道粮行。<br>
如鸟飞空，影则相随；若行圣行，得真乐行。

<script src="https://cdn.jsdelivr.net/gh/budaipro/assets@latest/amplitude.min.js"></script>
<script>
let songElements = document.getElementsByClassName('song');

for( var i = 0; i < songElements.length; i++ ){
	songElements[i].addEventListener('mouseover', function(){
		this.style.backgroundColor = '#00A0FF';
		this.querySelectorAll('.song-meta-data .song-title')[0].style.color = '#FFFFFF';
		this.querySelectorAll('.song-meta-data .song-artist')[0].style.color = '#FFFFFF';
		if( !this.classList.contains('amplitude-active-song-container') ){
			this.querySelectorAll('.play-button-container')[0].style.display = 'block';
		}
		this.querySelectorAll('.song-duration')[0].style.color = '#FFFFFF';
	});

	songElements[i].addEventListener('mouseout', function(){
		this.style.backgroundColor = '#FFFFFF';
		this.querySelectorAll('.song-meta-data .song-title')[0].style.color = '#272726';
		this.querySelectorAll('.song-meta-data .song-artist')[0].style.color = '#607D8B';
		this.querySelectorAll('.play-button-container')[0].style.display = 'none';
		this.querySelectorAll('.song-duration')[0].style.color = '#607D8B';
	});

	songElements[i].addEventListener('click', function(){
		this.querySelectorAll('.play-button-container')[0].style.display = 'none';
	});
}

/*
	Initializes AmplitudeJS
*/
Amplitude.init({
  "songs": [
		{
			"name": "布袋豆腐歌 trance版",
			"artist": "SUNO AI",
			"album": "布袋豆腐歌",
			"url": "https://cdn.jsdelivr.net/gh/budaipro/assets@latest/audio/%E5%B8%83%E8%A2%8B%E8%B1%86%E8%85%90%E6%AD%8C_trance.mp3",
			"cover_art_url": "https://cdn.jsdelivr.net/gh/budaipro/assets@latest/amplitude/cover.png"
		},
		{
			"name": "布袋豆腐歌 rock版",
			"artist": "SUNO AI",
			"album": "布袋豆腐歌",
			"url": "https://cdn.jsdelivr.net/gh/budaipro/assets@latest/audio/%E5%B8%83%E8%A2%8B%E8%B1%86%E8%85%90%E6%AD%8C_rock.mp3",
			"cover_art_url": "https://cdn.jsdelivr.net/gh/budaipro/assets@latest/amplitude/cover.png"
		}
  ],
  
  "callbacks": {
    'play': function() {
        document.getElementById('album-art').style.visibility = 'hidden';
        document.getElementById('large-visualization').style.visibility = 'visible';
    },

    'pause': function() {
        document.getElementById('album-art').style.visibility = 'visible';
        document.getElementById('large-visualization').style.visibility = 'hidden';
    }
  },

  waveforms: {
    sample_rate: 50
  }
});
</script>
<style>
/*
  2. Components
*/
div#amplitude-player {
  background: #FFFFFF;
  box-shadow: 0 2px 12px 8px rgba(0, 0, 0, 0.1);
  margin-top: 20px;
  margin-bottom: 20px;
  max-width: 330px;
  scale: .65; }
@media screen and (max-width: 39.9375em) {
  div#amplitude-player {} }
/* Medium only */
@media screen and (min-width: 40em) and (max-width: 63.9375em) {
  div#amplitude-player {} }
/* Large and up */
@media screen and (min-width: 64em) {
  div#amplitude-player {} }
div#amplitude-left {
  padding: 0px;
  border-right: 1px solid #CFD8DC;
  width: 100%;}
  div#amplitude-left img.album-art {
    width: 50%;
    display: block;
    margin: 0 auto; 
    display: none; }
  div#amplitude-left div#player-left-bottom {
    flex: 1;
    background-color: #F1F1F1;
    padding: 20px 10px; }
    div#amplitude-left div#player-left-bottom div#volume-container:after {
      content: "";
      display: table;
      clear: both; }
/* Small only */
@media screen and (max-width: 39.9375em) {
  div#amplitude-player div#amplitude-left {
    width: 100%; }
    div#amplitude-player div#amplitude-left img[amplitude-song-info="cover_art_url"] {
      width: auto;
      height: auto; } }
/* Small only */
div#progress-container {
  width: 70%;
  float: left;
  position: relative;
  height: 20px;
  cursor: pointer;
  /*
    IE 11
  */ }
  div#progress-container:hover input[type=range].amplitude-song-slider::-webkit-slider-thumb {
    display: block; }
  div#progress-container:hover input[type=range].amplitude-song-slider::-moz-range-thumb {
    visibility: visible; }
  div#progress-container progress#song-played-progress {
    width: 100%;
    position: absolute;
    left: 0;
    top: 8px;
    right: 0;
    width: 100%;
    z-index: 60;
    -webkit-appearance: none;
    -moz-appearance: none;
    appearance: none;
    height: 4px;
    border-radius: 5px;
    background: transparent;
    border: none;
    /* Needed for Firefox */ }
  @media all and (-ms-high-contrast: none) {
    div#progress-container *::-ms-backdrop, div#progress-container progress#song-played-progress {
      color: #00A0FF;
      border: none;
      background-color: #CFD8DC; } }
  @supports (-ms-ime-align: auto) {
    div#progress-container progress#song-played-progress {
      color: #00A0FF;
      border: none; } }
  div#progress-container progress#song-played-progress[value]::-webkit-progress-bar {
    background: none;
    border-radius: 5px; }
  div#progress-container progress#song-played-progress[value]::-webkit-progress-value {
    background-color: #00A0FF;
    border-radius: 5px; }
  div#progress-container progress#song-played-progress::-moz-progress-bar {
    background: none;
    border-radius: 5px;
    background-color: #00A0FF;
    height: 5px;
    margin-top: -2px; }
  div#progress-container progress#song-buffered-progress {
    position: absolute;
    left: 0;
    top: 8px;
    right: 0;
    width: 100%;
    z-index: 10;
    -webkit-appearance: none;
    -moz-appearance: none;
    appearance: none;
    height: 4px;
    border-radius: 5px;
    background: transparent;
    border: none;
    background-color: #D7DEE3; }
  div#progress-container progress#song-buffered-progress[value]::-webkit-progress-bar {
    background-color: #CFD8DC;
    border-radius: 5px; }
  div#progress-container progress#song-buffered-progress[value]::-webkit-progress-value {
    background-color: #78909C;
    border-radius: 5px;
    transition: width .1s ease; }
  div#progress-container progress#song-buffered-progress::-moz-progress-bar {
    background: none;
    border-radius: 5px;
    background-color: #78909C;
    height: 5px;
    margin-top: -2px; }
  div#progress-container progress::-ms-fill {
    border: none; }
@-moz-document url-prefix() {
  div#progress-container progress#song-buffered-progress {
    top: 9px;
    border: none; } }
  @media all and (-ms-high-contrast: none) {
    div#progress-container *::-ms-backdrop, div#progress-container progress#song-buffered-progress {
      color: #78909C;
      border: none; } }
  @supports (-ms-ime-align: auto) {
    div#progress-container progress#song-buffered-progress {
      color: #78909C;
      border: none; } }
  div#progress-container input[type=range] {
    -webkit-appearance: none;
    width: 100%;
    margin: 7.5px 0;
    position: absolute;
    z-index: 9999;
    top: -7px;
    height: 20px;
    cursor: pointer;
    background-color: inherit; }
  div#progress-container input[type=range]:focus {
    outline: none; }
  div#progress-container input[type=range]::-webkit-slider-runnable-track {
    width: 100%;
    height: 0px;
    cursor: pointer;
    box-shadow: 0px 0px 0px rgba(0, 0, 0, 0), 0px 0px 0px rgba(13, 13, 13, 0);
    background: #0075a9;
    border-radius: 0px;
    border: 0px solid #010101; }
  div#progress-container input[type=range]::-webkit-slider-thumb {
    box-shadow: 0px 0px 0px #000000, 0px 0px 0px #0d0d0d;
    border: 1px solid #00a0ff;
    height: 15px;
    width: 15px;
    border-radius: 16px;
    background: #00a0ff;
    cursor: pointer;
    -webkit-appearance: none;
    margin-top: -7.5px; }
  div#progress-container input[type=range]:focus::-webkit-slider-runnable-track {
    background: #00adfb; }
  div#progress-container input[type=range]::-moz-range-track {
    width: 100%;
    height: 0px;
    cursor: pointer;
    box-shadow: 0px 0px 0px rgba(0, 0, 0, 0), 0px 0px 0px rgba(13, 13, 13, 0);
    background: #0075a9;
    border-radius: 0px;
    border: 0px solid #010101; }
  div#progress-container input[type=range]::-moz-range-thumb {
    box-shadow: 0px 0px 0px #000000, 0px 0px 0px #0d0d0d;
    border: 1px solid #00a0ff;
    height: 15px;
    width: 15px;
    border-radius: 16px;
    background: #00a0ff;
    cursor: pointer; }
  div#progress-container input[type=range]::-ms-track {
    width: 100%;
    height: 0px;
    cursor: pointer;
    background: transparent;
    border-color: transparent;
    color: transparent; }
  div#progress-container input[type=range]::-ms-fill-lower {
    background: #003d57;
    border: 0px solid #010101;
    border-radius: 0px;
    box-shadow: 0px 0px 0px rgba(0, 0, 0, 0), 0px 0px 0px rgba(13, 13, 13, 0); }
  div#progress-container input[type=range]::-ms-fill-upper {
    background: #0075a9;
    border: 0px solid #010101;
    border-radius: 0px;
    box-shadow: 0px 0px 0px rgba(0, 0, 0, 0), 0px 0px 0px rgba(13, 13, 13, 0); }
  div#progress-container input[type=range]::-ms-thumb {
    box-shadow: 0px 0px 0px #000000, 0px 0px 0px #0d0d0d;
    border: 1px solid #00a0ff;
    height: 15px;
    width: 15px;
    border-radius: 16px;
    background: #00a0ff;
    cursor: pointer;
    height: 0px;
    display: block; }
  @media all and (-ms-high-contrast: none) {
    div#progress-container *::-ms-backdrop, div#progress-container input[type="range"].amplitude-song-slider {
      padding: 0px; }
    div#progress-container *::-ms-backdrop, div#progress-container input[type=range].amplitude-song-slider::-ms-thumb {
      height: 15px;
      width: 15px;
      border-radius: 10px;
      cursor: pointer;
      margin-top: -8px; }
    div#progress-container *::-ms-backdrop, div#progress-container input[type=range].amplitude-song-slider::-ms-track {
      border-width: 15px 0;
      border-color: transparent; }
    div#progress-container *::-ms-backdrop, div#progress-container input[type=range].amplitude-song-slider::-ms-fill-lower {
      background: #CFD8DC;
      border-radius: 10px; }
    div#progress-container *::-ms-backdrop, div#progress-container input[type=range].amplitude-song-slider::-ms-fill-upper {
      background: #CFD8DC;
      border-radius: 10px; } }
  @supports (-ms-ime-align: auto) {
    div#progress-container input[type=range].amplitude-song-slider::-ms-thumb {
      height: 15px;
      width: 15px;
      margin-top: 3px; } }
  div#progress-container input[type=range]:focus::-ms-fill-lower {
    background: #0075a9; }
  div#progress-container input[type=range]:focus::-ms-fill-upper {
    background: #00adfb; }
div#control-container {
  margin-top: 25px;
  margin-top: 20px; }
  div#control-container div#repeat-container {
    width: 25%;
    float: left;
    padding-top: 20px; }
    div#control-container div#repeat-container div#repeat {
      width: 24px;
      height: 19px;
      cursor: pointer; }
      div#control-container div#repeat-container div#repeat.amplitude-repeat-off {
        background: url("https://cdn.jsdelivr.net/gh/budaipro/assets@latest/amplitude/repeat-off.svg"); }
      div#control-container div#repeat-container div#repeat.amplitude-repeat-on {
        background: url("https://cdn.jsdelivr.net/gh/budaipro/assets@latest/amplitude/repeat-on.svg"); }
    div#control-container div#repeat-container div#shuffle {
      width: 23px;
      height: 19px;
      cursor: pointer;
      float: right; }
      div#control-container div#repeat-container div#shuffle.amplitude-shuffle-off {
        background: url("https://cdn.jsdelivr.net/gh/budaipro/assets@latest/amplitude/shuffle-off.svg"); }
      div#control-container div#repeat-container div#shuffle.amplitude-shuffle-on {
        background: url("https://cdn.jsdelivr.net/gh/budaipro/assets@latest/amplitude/shuffle-on.svg"); }
  @media all and (-ms-high-contrast: none) {
    div#control-container *::-ms-backdrop, div#control-container div#control-container {
      margin-top: 40px;
      float: none; } }
  div#control-container div#central-control-container {
    width: 50%;
    float: left; }
    div#control-container div#central-control-container div#central-controls {
      width: 130px;
      margin: auto; }
      div#control-container div#central-control-container div#central-controls div#previous {
        display: inline-block;
        width: 40px;
        height: 40px;
        cursor: pointer;
        background: url("https://cdn.jsdelivr.net/gh/budaipro/assets@latest/amplitude/prev.svg");
        background-repeat: no-repeat;
        float: left;
        margin-top: 10px;
        margin-right: -5px; }
      div#control-container div#central-control-container div#central-controls div#play-pause {
        display: inline-block;
        width: 60px;
        height: 60px;
        cursor: pointer;
        float: left; }
        div#control-container div#central-control-container div#central-controls div#play-pause.amplitude-paused {
          background: url("https://cdn.jsdelivr.net/gh/budaipro/assets@latest/amplitude/play.svg"); }
        div#control-container div#central-control-container div#central-controls div#play-pause.amplitude-playing {
          background: url("https://cdn.jsdelivr.net/gh/budaipro/assets@latest/amplitude/pause.svg"); }
      div#control-container div#central-control-container div#central-controls div#next {
        display: inline-block;
        width: 40px;
        height: 40px;
        cursor: pointer;
        background: url("https://cdn.jsdelivr.net/gh/budaipro/assets@latest/amplitude/next.svg");
        background-repeat: no-repeat;
        float: left;
        margin-top: 10px;
        margin-left: -5px; }
  div#control-container div#volume-container {
    width: 25%;
    float: left;
    padding-top: 20px; }
    div#control-container div#volume-container div#shuffle-right {
      width: 23px;
      height: 19px;
      cursor: pointer;
      margin: auto; }
      div#control-container div#volume-container div#shuffle-right.amplitude-shuffle-off {
        background: url("https://cdn.jsdelivr.net/gh/budaipro/assets@latest/amplitude/shuffle-off.svg"); }
      div#control-container div#volume-container div#shuffle-right.amplitude-shuffle-on {
        background: url("https://cdn.jsdelivr.net/gh/budaipro/assets@latest/amplitude/shuffle-on.svg"); }
  div#control-container div.amplitude-mute {
    cursor: pointer;
    width: 25px;
    height: 19px;
    float: left; }
    div#control-container div.amplitude-mute.amplitude-not-muted {
      background: url("https://cdn.jsdelivr.net/gh/budaipro/assets@latest/amplitude/volume.svg");
      background-repeat: no-repeat; }
    div#control-container div.amplitude-mute.amplitude-muted {
      background: url("https://cdn.jsdelivr.net/gh/budaipro/assets@latest/amplitude/mute.svg");
      background-repeat: no-repeat; }
div#control-container:after {
  content: "";
  display: table;
  clear: both; }
/* Small only */
@media screen and (max-width: 39.9375em) {
  div#amplitude-player div#repeat-container div#repeat {
    margin-left: auto;
    margin-right: auto;
    float: none; }
  div#amplitude-player div#repeat-container div#shuffle {
    display: none; }
  div#amplitude-player div#volume-container div.volume-controls {
    display: none; }
  div#amplitude-player div#volume-container div#shuffle-right {
    display: block; } }
/* Medium only */
@media screen and (min-width: 40em) and (max-width: 63.9375em) {
  div#amplitude-player div#repeat-container div#repeat {
    margin-left: auto;
    margin-right: auto;
    float: none; }
  div#amplitude-player div#repeat-container div#shuffle {
    display: none; }
  div#amplitude-player div#volume-container div.volume-controls {
    display: none; }
  div#amplitude-player div#volume-container div#shuffle-right {
    display: block; } }
/* Large and up */
@media screen and (min-width: 64em) {
  div#amplitude-player div#repeat-container div#repeat {
    margin-left: 10px;
    margin-right: 20px;
    float: left; }
  div#amplitude-player div#volume-container div#shuffle-right {
    display: none; } }
input[type=range].amplitude-volume-slider {
  -webkit-appearance: none;
  width: calc( 100% - 33px);
  float: left;
  margin-top: 10px;
  margin-left: 5px; }
@-moz-document url-prefix() {
  input[type=range].amplitude-volume-slider {
    margin-top: 0px; } }
@supports (-ms-ime-align: auto) {
  input[type=range].amplitude-volume-slider {
    margin-top: 3px;
    height: 12px;
    background-color: rgba(255, 255, 255, 0) !important;
    z-index: 999;
    position: relative; }
  div.ms-range-fix {
    height: 1px;
    background-color: #A9A9A9;
    width: 67%;
    float: right;
    margin-top: -6px;
    z-index: 9;
    position: relative; } }
@media all and (-ms-high-contrast: none) {
  *::-ms-backdrop, input[type=range].amplitude-volume-slider {
    margin-top: -24px;
    background-color: rgba(255, 255, 255, 0) !important; } }
input[type=range].amplitude-volume-slider:focus {
  outline: none; }
input[type=range].amplitude-volume-slider::-webkit-slider-runnable-track {
  width: 75%;
  height: 1px;
  cursor: pointer;
  animate: 0.2s;
  background: #CFD8DC; }
input[type=range].amplitude-volume-slider::-webkit-slider-thumb {
  height: 10px;
  width: 10px;
  border-radius: 10px;
  background: #00A0FF;
  cursor: pointer;
  margin-top: -4px;
  -webkit-appearance: none; }
input[type=range].amplitude-volume-slider:focus::-webkit-slider-runnable-track {
  background: #CFD8DC; }
input[type=range].amplitude-volume-slider::-moz-range-track {
  width: 100%;
  height: 1px;
  cursor: pointer;
  animate: 0.2s;
  background: #CFD8DC; }
input[type=range].amplitude-volume-slider::-moz-range-thumb {
  height: 10px;
  width: 10px;
  border-radius: 10px;
  background: #00A0FF;
  cursor: pointer;
  margin-top: -4px; }
input[type=range].amplitude-volume-slider::-ms-track {
  width: 100%;
  height: 1px;
  cursor: pointer;
  animate: 0.2s;
  background: transparent;
  /*leave room for the larger thumb to overflow with a transparent border */
  border-color: transparent;
  border-width: 15px 0;
  /*remove default tick marks*/
  color: transparent; }
input[type=range].amplitude-volume-slider::-ms-fill-lower {
  background: #CFD8DC;
  border-radius: 10px; }
input[type=range].amplitude-volume-slider::-ms-fill-upper {
  background: #CFD8DC;
  border-radius: 10px; }
input[type=range].amplitude-volume-slider::-ms-thumb {
  height: 10px;
  width: 10px;
  border-radius: 10px;
  background: #00A0FF;
  cursor: pointer;
  margin-top: 2px; }
input[type=range].amplitude-volume-slider:focus::-ms-fill-lower {
  background: #CFD8DC; }
input[type=range].amplitude-volume-slider:focus::-ms-fill-upper {
  background: #CFD8DC; }
input[type=range].amplitude-volume-slider::-ms-tooltip {
  display: none; }
div#time-container span.current-time {
  color: #607D8B;
  font-size: 14px;
  font-weight: 700;
  float: left;
  width: 15%;
  text-align: center; }
div#time-container span.duration {
  color: #607D8B;
  font-size: 14px;
  font-weight: 700;
  float: left;
  width: 15%;
  text-align: center; }
div#time-container:after {
  content: "";
  display: table;
  clear: both; }
div#meta-container {
  text-align: center;
  margin-top: 5px; }
  div#meta-container span.song-name {
    display: block;
    color: #272726;
    font-size: 20px;
    font-family: 'Open Sans', sans-serif;
    white-space: nowrap;
    overflow: hidden;
    text-overflow: ellipsis; }
  div#meta-container div.song-artist-album {
    color: #607D8B;
    font-size: 14px;
    font-weight: 700;
    text-transform: uppercase;
    font-family: 'Open Sans', sans-serif;
    white-space: nowrap;
    overflow: hidden;
    text-overflow: ellipsis; 
    display: none; }
    div#meta-container div.song-artist-album span {
      display: block; }
/*
  3. Layout
*/
body {
  background-image: -webkit-linear-gradient(316deg, #3BD2AE 0%, #36BAC2 100%);
  background-image: linear-gradient(-226deg, #3BD2AE 0%, #36BAC2 100%);
  height: 100vh;
  -webkit-font-smoothing: antialiased;
  font-family: "Helvetica Neue",Helvetica,Roboto,Arial,sans-serif;
  line-height: 1.5; }
div.amplitude-wave-form{
    display: none;
    margin-top: -14px;
}    
 div.amplitude-wave-form svg{
      stroke: #00a0ff;
      height: 50px;
      width: 100%;
      stroke-width: .5px;
}
 div.amplitude-wave-form svg g{
   stroke: #00a0ff;
   height: 50px;
   width: 100%;
}
 div.amplitude-wave-form svg g path{
   stroke: #00a0ff;
   height: 50px;
   width: 100%;
}
div#large-visualization{
    width: 100%;
    background-color: black;
    visibility: hidden;
  }
</style>