<script>
  export let Person = {};
</script>

<div
  class="row w3-panel w3-card-4 w3-cell-row w3-mobile"
  style="min-height:65px;"
>
  <div class="avatar w3-cell w3-cell-middle w3-center " style="width:10%;">
    <img
      class="w3-circle w3-hide-small"
      style="width:50px; height:50px;"
      src={Person.avatar}
      alt="Profile Avatar"
    />
  </div>

  <div
    class="cell w3-cell w3-cell-middle w3-mobile w3-border-left"
    style="width:30%;"
  >
    {Person.name}
  </div>
  <div
    class="cell w3-cell w3-cell-middle w3-mobile w3-border-left"
    style="width:20%;"
  >
    {Person.phone}
  </div>
  <div
    class="cell w3-cell w3-cell-middle w3-mobile w3-border-left"
    style="width:40%;"
  >
    {Person.email}
  </div>
</div>

<style>
  @media screen and (max-width: 640px) {
    .row {
      padding: 10px;
    }
    .cell {
      padding-bottom: 5px;
    }
    .avatar {
      display: none;
    }
    .cell {
      border: none;
    }
  }
  .cell {
    overflow-x: auto;
  }
  .row:hover {
    background-color: #cecece;
    cursor: pointer;
  }
</style>
