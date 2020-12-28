<template>
  <b-container>
    <div class="my-3">
      <h1 class="text-center">Goods</h1>
      <b-button href="/Add">Add</b-button>
    </div>
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
          { UID:10, number_of_stack: 1, Name: 'Ayam Bawang', Recipe: 'ayam, bawang', used_by: 'Andy', user_id: 'u1', batch_number: 'X1' },
          { UID:20, number_of_stack: 2, Name: 'Ayam Geprek', Recipe: 'ayam, cabe', used_by: 'Budi', user_id: 'u2', batch_number: 'X2' },
          { UID:30, number_of_stack: 3, Name: 'Ayam Bakar', Recipe: 'ayam, kecap', used_by: 'Dona', user_id: 'u3', batch_number: 'X3' },
          { UID:40, number_of_stack: 4, Name: 'Ayam Goreng', Recipe: 'ayam, minyak', used_by: 'Dodi', user_id: 'u4', batch_number: 'X4' }
        ]
      }
    }
};
</script>
