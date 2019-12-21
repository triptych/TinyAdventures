<script>
  // import Button from "./Button.svelte";
  import Field from "./components/Field.svelte";
  import Controls from "./components/Controls.svelte";
  let name = "Barry The Barbarian";
  let ran = ["A giant monster", "A treasure", "A friend"];

  let txt = "loading...";

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

  function handleDirection(event) {
    console.log("handleDirection:", event.detail.text);
    txt = event.detail.text;
  }
</script>

<style>
	header,
	main,
	footer {
	  font-family: sans-serif;
	}
</style>

<header>
<h1>
	A Tiny Adventure
	</h1>
</header>
<main>
	<!-- <div class="display">{name}</div> -->
	<Field text={txt}/>
<Controls on:direction={handleDirection}/>
	
	<div>
		<button on:click={updateMessage}>
			next
		</button>
	</div>
</main>
<footer>
By Andrew Wooldridge
</footer>