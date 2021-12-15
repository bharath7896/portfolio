# portfolio.github.io
<!DOCTYPE html>
<html>
    <head>
        <title>Samaritan</title>
        <meta charset="UTF-8">
        <meta name="theme-color" content="#000000">
        <meta name="apple-mobile-web-app-capable" content="yes">
        <link rel="icon" sizes="192x192" href="./img/icon.png">
		<link rel="manifest" href="./manifest.json">
        <meta name="viewport" content="width=device-width, user-scalable=no, initial-scale=1.0">
        <script type="text/javascript" src="./js/jquery-1.11.0.min.js"></script>
        <script type="text/javascript" src="./js/velocity.min.js"></script>
        <script type="text/javascript" src="./js/screenfull.min.js"></script>
        <script type="text/javascript" src="./js/phraselist.js"></script>
        <script type="text/javascript" src="./js/samaritan.js"></script>
        <script type="text/javascript" src="./js/annyang.min.js"></script>
        <script type="text/javascript" src="./js/speech.js"></script>
        <script type="text/javascript" src="./js/main.js"></script>
        <link rel="stylesheet" type="text/css" href="./css/style.css">
    </head>
    <body>
		<div id="boot-screen" style="margin: 0; height:100vh; pointer-events: none;">
			<div id="boot-video"></div>
			<script>
				var tag = document.createElement('script');
				tag.src = "https://www.youtube.com/player_api";

				var firstScriptTag = document.getElementsByTagName('script')[0];
				firstScriptTag.parentNode.insertBefore(tag, firstScriptTag);

				var player;

				function onYouTubePlayerAPIReady() {
					player = new YT.Player('boot-video', {
						height: '100%',
						width: '100%',
						videoId: 'xHAzhkIt0z4',
						playerVars: {
							rel: 0,
							autoplay: 1,
							showinfo: 0,
							iv_load_policy: 3,
							controls: 0,
							modestbranding: 1,
							enablejsapi: 1
						},
						events: {
							'onReady': onPlayerReady,
						}
					});
				}

				function onPlayerReady(event) {
					event.target.mute();
				}
			</script>
		</div>
        <div id="interface">
			<div id="main">
				<p>&nbsp;</p>
				<hr />
			</div>
			<div id="marker">
				<span id="triangle">&#9650</span>
			</div>
        </div>
    </body>
</html>
