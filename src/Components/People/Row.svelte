<script>
  export let peopleList = [];

  function enableDelete(id) {
    console.log(id);
  }
</script>

{#each peopleList as people (people.id)}
  <div
    on:mouseenter={enableDelete(people.id)}
    class="w3-block w3-border w3-border-blue w3-card-4 w3-section w3-cell-row  w3-mobile w3-padding"
  >
    <div class="w3-cell w3-padding w3-center" style="width:10%;">
      <img
        class="w3-circle w3-hide-small w3-mobile"
        src={people.avatar}
        alt="Profile Avatar"
        style="width:60px; max-height:60px;"
      />
    </div>
    <div class="w3-cell w3-border-left w3-padding " style="width:35%;">
      {people.name}
    </div>
    <div class="w3-cell w3-border-left w3-padding " style="widht:55%;">
      {people.address.country}, {people.address.city}, {people.address.state}, {people
        .address.streetA}, {people.address.zipcode}
    </div>

    <div class="delete" style="font-size:50px; color:red;">-</div>
  </div>
{/each}

<style>
  div:hover {
    background-color: #cecece;
    cursor: pointer;
  }
  .delete:hover {
    visibility: visible;
  }
</style>
