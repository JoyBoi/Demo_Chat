<template>
  <b-container fluid class="welcome">
    <b-card
      bg-variant="light"
      text-variant="primary"
      title="Welcome"
      title-tag="h1"
      class="text-center"
    >
      <div class="text-dark">
        <b-form @submit="onSubmit" @reset="onReset">
          <b-form-group
            id="input-group-1"
            label="User Name:"
            label-for="input-1"
            label-size="sm"
            class="text-left font-weight-lighter"
          >
            <b-form-input
              id="input-1"
              v-model="form.username"
              placeholder="Enter Name"
              required
            >
            </b-form-input>
          </b-form-group>
          <b-form-group
            id="input-group-2"
            label="Room Name:"
            label-for="input-2"
            label-size="sm"
            class="text-left font-weight-lighter"
          >
            <b-form-select
              id="input-2"
              v-model="form.roomname"
              :options="rooms"
              required
            ></b-form-select>
          </b-form-group>
          <b-button type="submit" variant="primary">Submit</b-button>
          <b-button type="reset" variant="danger">Reset</b-button>
        </b-form>
      </div>
    </b-card>
  </b-container>
</template>

<script>
export default {
  data() {
    return {
      form: {
        username: "",
        roomname: null,
      },
      rooms: [
        { text: "Select Chat-Room", value: null },
        "VueJS",
        "ReactJS",
        "Svelte",
        "Angular",
      ],
    };
  },
  methods: {
    onSubmit(event) {
      event.preventDefault();
      alert(JSON.stringify(this.form));
    },
    onReset(event) {
      event.preventDefault();
      this.form.username = "";
      this.form.roomname = "";
    },
  },
};
</script>

<style scoped>
.welcome {
  max-width: 500px;
  margin-top: 100px;
}
.welcome button {
  margin: 30px 35px;
}
</style>