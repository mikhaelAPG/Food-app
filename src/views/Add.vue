<template>
  <b-container>
    <div class="my-3">
      <h1 class="text-center mt-5">Add User</h1>
        </div>
        <div>
        <div>
        <b-form @submit="onSubmit" @reset="onReset" v-if="show" class="w-50">
        <b-form-group
            id="input-group-1"
            label="Email address:"
            label-for="input-1"
            description="We'll never share your email with anyone else."
        >
            <b-form-input
            id="input-1"
            v-model="form.email"
            type="email"
            placeholder="Enter email"
            required
            ></b-form-input>
        </b-form-group>

        <b-form-group id="input-group-2" label="Your Name:" label-for="input-2">
            <b-form-input
            id="input-2"
            v-model="form.name"
            placeholder="Enter name"
            type="text"
            required
            ></b-form-input>
        </b-form-group>

        <b-form-group id="input-group-3" label="Your Password:" label-for="input-3">
            <b-form-input
            id="input-3"
            v-model="form.password"
            type="password"
            required
            ></b-form-input>
        </b-form-group>

        <b-button type="submit" variant="primary">Submit</b-button>
        <b-button type="reset" variant="danger" class="ml-3">Cancel</b-button>
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
