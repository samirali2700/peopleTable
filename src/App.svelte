<script>
  import PeopleTable from "./Components/People/PeopleTable.svelte";
</script>

<main class="w3-container  w3-section w3-auto" style="max-width:1150px;">
  <PeopleTable />
</main>

<style>
  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>
