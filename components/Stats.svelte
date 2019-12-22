<script>
let hp = 100;
let mana = 100;
let gold = 0;
</script>
<style>
  .stats-display {
    display: flex;
    flex-direction: column;
    justify-content: space-around;
    width: 100%;
    border: 1px dotted green;
    padding: 4px;
  }
</style>
<div class="stats-display">
  <div>HP: {hp}</div>
  <div>Mana: {mana}</div>
  <div>Gold: {gold}</div>
</div>