<script>
  // import Button from "./Button.svelte";
  import Field from "./components/Field.svelte";
  import Controls from "./components/Controls.svelte";
  import Stats from "./components/Stats.svelte";
  import Row from "./components/Row.svelte";

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
<Field dir={txt}/>

<Row>
  <div slot="left">
    <Controls on:direction={handleDirection} />
  </div>
  <div slot="right">
    <Stats/>
  </div>
</Row>
</main>
<footer>
By Andrew Wooldridge
</footer>