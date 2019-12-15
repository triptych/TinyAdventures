<script>
 // import Button from "./Button.svelte";
 let name = "Barry The Barbarian";
 let ran = ["A giant monster", "A treasure", "A friend"];

 function updateMessage() {
   // let num = Math.floor(Math.random() * random.length);
   // console.log("updatemessge: " + num);
   // name = ran[num];
   // console.log("name:" + name);
   console.log("hi");
   let num = Math.floor(Math.random() * ran.length);
   //name = ran[0];
   console.log("num:" + num);
   console.log("updatemessge: " + num);
   name = ran[num];
 }
 function goUp() {
   console.log("goup");
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

<style>
	header,
	main,
	footer {
	  font-family: sans-serif;
	}

	.display {
	  width: 1fw;
	  height: 100px;
	  border: 1px solid black;
	}
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

<header>
<h1>
	A Tiny Adventure
	</h1>
</header>
<main>
	<div class="display">{name}</div>

	<div class="interface">
		<div class="up" on:click={goUp}>up</div>
		<div class="down" on:click={goDown}>down</div>
		<div class="left" on:click={goLeft}>left</div>
		<div class="right" on:click={goRight}>right</div>
	
	</div>
	<div>
		<button on:click={updateMessage}>
			next
		</button>
	</div>
</main>
<footer>
By Andrew Wooldridge
</footer>