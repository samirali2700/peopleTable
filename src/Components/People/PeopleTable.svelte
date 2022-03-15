<script>
  import Head from "./Head.svelte";
  import Row from "./Row.svelte";

  export let peopleList = [];
  console.log(Element.clientWidth);
</script>

<div class="w3-container w3-border w3-mobile">
  <div class="mm">
    <Head />
  </div>

  {#each peopleList as people (people.id)}
    <Row Person={people} />
  {/each}
</div>

<style>
  @media screen and (max-width: 650px) {
    .mm {
      display: none;
    }
  }
</style>
