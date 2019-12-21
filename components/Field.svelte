<div class="field-display">
	{text}
</div>
<style>
	.field-display {
	  width: 1fw;
	  height: 100px;
	  border: 1px solid black;
	}
</style>
<script>
	export let text;
	$: {
	  console.log(`field: the text is ${text}`);
	}
</script>