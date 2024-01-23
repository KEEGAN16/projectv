<template>
  <div class="registration-form">
    <h2 class="heading">Registrácia</h2>

    <form @submit.prevent="submitForm">
      <div class="form-group">
        <label for="email">Email:</label>
        <input type="email" id="email" v-model="email" required class="form-control" />
      </div>

      <div class="form-group">
        <label for="password">Heslo:</label>
        <input type="password" id="password" v-model="password" required class="form-control" />
      </div>

      <div class="form-group">
        <label for="firstName">Krstné meno:</label>
        <input type="text" id="firstName" v-model="firstName" required class="form-control" />
      </div>

      <div class="form-group">
        <label for="lastName">Priezvisko:</label>
        <input type="text" id="lastName" v-model="lastName" required class="form-control" />
      </div>

      <button type="submit" class="btn btn-primary">Register</button>
    </form>
  </div>
</template>

<script>
export default {
  data() {
    return {
      email: '',
      password: '',
      firstName: '',
      lastName: ''
    }
  },
  methods: {
    submitForm() {
      console.log('Registration:', this.email, this.password, this.firstName, this.lastName)
    }
  }
}
</script>

<style scoped>
.registration-form {
  background-color: #fff;
  padding: 2rem;
  border-radius: 5px;
  margin: 0 auto;
  width: 500px;
}

.heading {
  text-align: center;
  margin-bottom: 20px;
  font-size: 2em;
  font-weight: 700;
}

.form-group {
  margin-bottom: 10px;
}

.form-control {
  width: 100%;
  padding: 8px;
  border: 1px solid #ccc;
}

.btn {
  padding: 10px;
  background-color: #007bff;
  color: #fff;
  border: none;
  cursor: pointer;
  border-radius: 5px;
}
</style>
