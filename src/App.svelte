<script>
  import PeopleTable from "./Components/People/PeopleTable.svelte";

  import { faker } from "@faker-js/faker";
  faker.setLocale("nb_NO");

  let peopleList = [];

  for (let i = 0; i < 10; i++) {
    let Person = faker.helpers.createCard();
    let Temp = (peopleList = [
      ...peopleList,
      {
        id: i,
        avatar: faker.image.avatar(),
        name: Person.name,
        phone: Person.phone,
        email: Person.email,
      },
    ]);
  }
</script>

<main>
  <PeopleTable {peopleList} />
</main>

<style>
  main {
    text-align: center;
    padding: 1em;

    margin: 0 auto;
  }

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>
