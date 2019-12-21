<style>
	.interface {
	  display: grid;
	  border: 1px solid #2d2d2d;
	  border-radius: 2px;
	  width: 50vw;
	  grid-template-columns: [colleft] auto [colcenter] auto [colright] auto;
	  grid-template-rows: [rowtop] auto [rowcenter] auto [rowbottom] auto;
	  justify-items: center;
	  align-items: center;
	}

	.interface div {
	  border: 1px solid tan;
	  padding: 2px;
	  cursor: pointer;
	}

	.interface div:hover {
	  color: white;
	  background-color: black;
	  border: 1px solid white;
	}

	.up {
	  grid-column-start: 2;
	}
	.down {
	  grid-column-start: 2;
	  grid-row-start: 3;
	}
	.left {
	  grid-column-start: 1;
	}
	.right {
	  grid-column-start: 3;
	}
</style>
<script>
  import { createEventDispatcher } from "svelte";

  const dispatch = createEventDispatcher();

  function goUp() {
    console.log("goup");
    dispatch("direction", {
      text: "Hello!"
    });
  }
  function goDown() {
    console.log("godown");
  }

  function goLeft() {
    console.log("goLeft");
  }

  function goRight() {
    console.log("goRight");
  }
</script>

<div class="interface">
		<div class="up" on:click={goUp}>up</div>
		<div class="down" on:click={goDown}>down</div>
		<div class="left" on:click={goLeft}>left</div>
		<div class="right" on:click={goRight}>right</div>
	
	</div>