<!DOCTYPE html>
<!--
	NOTES:
	1. All tokens are represented by '$' sign in the template.
	2. You can write your code only wherever mentioned.
	3. All occurrences of existing tokens will be replaced by their appropriate values.
	4. Blank lines will be removed automatically.
	5. Remove unnecessary comments before creating your template.
-->
<html>
<head>
<meta charset="UTF-8">
<meta name="authoring-tool" content="Adobe_Animate_CC">
<title>IMY120 - NormalExam - memo</title>
<!-- write your code here -->
<script src="libs/1.0.0/createjs.min.js"></script>
<script src="IMY120 - NormalExam - memo.js?1669277240279"></script>
<script>
var canvas, stage, exportRoot, anim_container, dom_overlay_container, fnStartAnimation;
function init() {
	canvas = document.getElementById("canvas");
	anim_container = document.getElementById("animation_container");
	dom_overlay_container = document.getElementById("dom_overlay_container");
	var comp=AdobeAn.getComposition("7197C4AD10BE864994175E8D3B74D77C");
	var lib=comp.getLibrary();
	handleComplete({},comp);
}
function handleComplete(evt,comp) {
	//This function is always called, irrespective of the content. You can use the variable "stage" after it is created in token create_stage.
	var lib=comp.getLibrary();
	var ss=comp.getSpriteSheet();
	exportRoot = new lib.IMY120NormalExammemo();
	stage = new lib.Stage(canvas);	
	//Registers the "tick" event listener.
	fnStartAnimation = function() {
		stage.addChild(exportRoot);
		createjs.Ticker.framerate = lib.properties.fps;
		createjs.Ticker.addEventListener("tick", stage);
	}	    
	//Code to support hidpi screens and responsive scaling.
	AdobeAn.makeResponsive(false,'both',false,1,[canvas,anim_container,dom_overlay_container]);	
	AdobeAn.compositionLoaded(lib.properties.id);
	fnStartAnimation();
}
</script>
<!-- write your code here -->
</head>
<body onload="init();" style="margin:0px;">
	<div id="animation_container" style="background-color:rgba(204, 204, 204, 1.00); width:1388px; height:909px">
		<canvas id="canvas" width="1388" height="909" style="position: absolute; display: block; background-color:rgba(204, 204, 204, 1.00);"></canvas>
		<div id="dom_overlay_container" style="pointer-events:none; overflow:hidden; width:1388px; height:909px; position: absolute; left: 0px; top: 0px; display: block;">
		</div>
	</div>
</body>
</html>
