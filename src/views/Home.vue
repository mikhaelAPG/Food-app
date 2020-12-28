<template>
  <b-container>
    <div>
      <b-table striped hover :items="items"></b-table>
    </div>
  </b-container>
</template>

<script>
// @ is an alias to /src

export default {
  /* name: "Home",
  components: {
  } */
  data() {
      return {
        items: [
          { UID:1, age: 40, first_name: 'Dickerson', last_name: 'Macdonald' },
          { UID:2, age: 21, first_name: 'Larsen', last_name: 'Shaw' },
          { UID:3, age: 89, first_name: 'Geneva', last_name: 'Wilson' },
          { UID:4, age: 38, first_name: 'Jami', last_name: 'Carney' }
        ]
      }
    }
};
</script>
