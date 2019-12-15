<script>
  import Button from "./Button.svelte";
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
</style>

<header>
<h1>
	A Tiny Adventure
	</h1>
</header>
<main>
	<div class="display">{name}</div>
	<div>
		<button on:click={updateMessage}>
			next
		</button>
	</div>
</main>
<footer>
By Andrew Wooldridge
</footer>