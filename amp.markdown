---
layout: default
title: "主页"
---

### 《布袋豆腐歌》

{%- include amplitude.html -%}

<script>
let songElements = document.getElementsByClassName('song');

for( var i = 0; i < songElements.length; i++ ) {
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
