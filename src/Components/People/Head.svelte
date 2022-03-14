<script>
  export let listLength;
</script>

<div class="w3-block w3-cell-row w3-border w3-border-blue  w3-padding">
  <div class="w3-cell" style="width:10%; ">
    {listLength === 0 ? "No User" : listLength === 1 ? "User:" : "Users:"}
    {#if listLength > 0}
      {listLength}
    {/if}
  </div>
  <div class="w3-cell w3-padding w3-border-left w3-center" style="width:35%; ">
    Name
  </div>
  <div class="w3-cell w3-padding w3-center w3-border-left" style="width:55%; ">
    Address
  </div>
</div>

<style>
</style>
