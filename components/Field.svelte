<div class="field-display">
	{text}
</div>
Going: {dir.split("|")[0]}. {err}. Steps: {steps}
<style>
	.field-display {
	  width: 1fw;
	  height: 100px;
	  border: 1px solid black;
	}
</style>
<script>
	let loc = {
	  x: 1,
	  y: 1
	};
	let text = "loading";
	let err = "";
	let steps = 0;
	const world = [
	  ["forest", "forest wall", "mountain"],
	  ["cliff", "meadow", "spring"],
	  ["hut", "fence", "castle"]
	];

	export let dir;
	$: {
	  //console.log(`field: the text is ${dir}`);
	  err = "You continue on your journey";
	  steps = dir.split("|")[1] ? dir.split("|")[1] : 0;
	  switch (dir.split("|")[0]) {
	    case "north":
	      if (loc.y > 0) {
	        loc.y -= 1;
	      } else {
	        err = "you can't go any further";
	      }
	      break;
	    case "south":
	      if (loc.y < world[0].length - 1) {
	        loc.y += 1;
	      } else {
	        err = "you can't go any further";
	      }
	      break;
	    case "west":
	      if (loc.x > 0) {
	        loc.x -= 1;
	      } else {
	        err = "you can't go any further";
	      }
	      break;
	    case "east":
	      if (loc.x < world.length - 1) {
	        loc.x += 1;
	      } else {
	        err = "you can't go any further";
	      }
	      break;
	  }
	  showLoc(loc);
	}

	function showLoc(location) {
	  text = world[location.y][location.x];
	}
</script>