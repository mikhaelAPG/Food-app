<template>
  <b-container>
    <div class="my-3">
      <h1 class="text-center mt-5">Add Goods</h1>
        </div>
        <div>
        <div>
        <b-form @submit="onSubmit" @reset="onReset" v-if="show" class="w-50">

        <b-form-group id="input-group-2" label="Item Name:" label-for="input-1">
            <b-form-input
            id="input-1"
            v-model="form.name"
            placeholder="Enter item name"
            type="text"
            required
            ></b-form-input>
        </b-form-group>

        <b-form-group id="input-group-2" label="Number of Stock:" label-for="input-2">
            <b-form-input
            id="input-2"
            v-model="form.stock"
            placeholder="Enter Number of Stock"
            type="text"
            required
            ></b-form-input>
        </b-form-group>

        <b-form-group id="input-group-3" label="Ingredient 1:" label-for="input-3">
        <b-form-select
          id="input-3"
          v-model="form.food"
          :options="foods"
          required
        ></b-form-select>
        </b-form-group>

        <b-form-group id="input-group-3" label="Ingredient 2:" label-for="input-4">
        <b-form-select
          id="input-4"
          v-model="form.food"
          :options="foods"
          required
        ></b-form-select>
        </b-form-group>

        <b-form-group id="input-group-3" label="Ingredient 3:" label-for="input-5">
        <b-form-select
          id="input-5"
          v-model="form.food"
          :options="foods"
          required
        ></b-form-select>
        </b-form-group>

        <b-button type="submit" variant="primary">Submit</b-button>
        <b-button variant="danger" class="ml-3" href="/cancel">Cancel</b-button>
        </b-form>
    </div>
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
        form: {
          email: '',
          name: '',
          food: null,
          checked: []
        },
        foods: [{ text: 'Select One', value: null }, 'Carrots', 'Beans', 'Tomatoes', 'Corn'],
        show: true
      }
    },
    methods: {
      onSubmit(event) {
        event.preventDefault()
        alert(JSON.stringify(this.form))
      },
      onReset(event) {
        event.preventDefault()
        // Reset our form values
        this.form.email = ''
        this.form.name = ''
        this.form.food = null
        this.form.checked = []
        // Trick to reset/clear native browser form validation state
        this.show = false
        this.$nextTick(() => {
          this.show = true
        })
      }
    }
};
</script>
