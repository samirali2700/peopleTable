<script>
  import Body from "./Body.svelte";
  import Head from "./Head.svelte";

  import { faker } from "@faker-js/faker";

  let peopleList = [];

  for (let i = 0; i < 10; i++) {
    let randomObject = faker.helpers.createCard();
    peopleList = [
      ...peopleList,
      {
        id: i,
        avatar: faker.image.avatar(),
        name: randomObject.name,
        address: randomObject.address,
      },
    ];
  }
</script>

<div
  class="w3-container w3-border w3-border-blue w3-card-2"
  style="padding:25px;"
>
  <Head listLength={peopleList.length} />
  <Body {peopleList} />
</div>

<style>
</style>
