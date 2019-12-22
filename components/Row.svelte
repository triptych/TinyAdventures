<style>
  .row-container {
    display: flex;
  }
</style>
<div class="row-container">
<div class="row-item-left">
  <slot name="left"></slot>
  </div>
  <div class="row-item-right">
<slot name="right"></slot>
</div>
</div>