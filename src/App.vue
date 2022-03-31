<template>
  <div id="app" class="container p-5">
    <accordion
        :id="accordionOptions.id"
        :flush="accordionOptions.isFlushed"
        :always-open="accordionOptions.alwaysOpen"
        :items="accordionOptions.posts"
    >
    </accordion>
  </div>
</template>

<script>

import Accordion from "./components/Accordion";
export default {
  name: 'App',
  components: {
    Accordion
  },
  data(){
    return {
      accordionOptions:{
        alwaysOpen: true,
        id: 'accordionExample',
        isFlushed: false,
        posts: [
          {
            "userId": 1,
            "id": 1,
            "title": "sunt aut facere repellat provident occaecati excepturi optio reprehenderit",
            "body": "quia et suscipit\nsuscipit recusandae consequuntur expedita et cum\nreprehenderit molestiae ut ut quas totam\nnostrum rerum est autem sunt rem eveniet architecto"
          },
          {
            "userId": 1,
            "id": 2,
            "title": "qui est esse",
            "body": "est rerum tempore vitae\nsequi sint nihil reprehenderit dolor beatae ea dolores neque\nfugiat blanditiis voluptate porro vel nihil molestiae ut reiciendis\nqui aperiam non debitis possimus qui neque nisi nulla"
          },
          {
            "userId": 1,
            "id": 3,
            "title": "ea molestias quasi exercitationem repellat qui ipsa sit aut",
            "body": "et iusto sed quo iure\nvoluptatem occaecati omnis eligendi aut ad\nvoluptatem doloribus vel accusantium quis pariatur\nmolestiae porro eius odio et labore et velit aut"
          },
        ]
      },
    }
  }
}
</script>

<style>

</style>
