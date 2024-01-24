<template>
  <form class="container" @submit.prevent="submitForm">
    <div class="mb-3">
      <label for="name" class="form-label">Name</label>
      <input type="text" class="form-control" id="name" aria-describedby="name" v-model="name">
    </div>
    <div class="mb-3">
      <label for="email" class="form-label">Email address</label>
      <input type="email" class="form-control" id="email" aria-describedby="email" v-model="email">
      <div id="emailHelp" class="form-text">We'll never share your email with anyone else.</div>
    </div>
    <div class="mb-3">
      <label for="address" class="form-label">address</label>
      <input type="text" class="form-control" id="address" v-model="address">
    </div>
    <div class="mb-3">
      <label for="message" class="form-label">message</label>
      <textarea class="form-control" id="message" v-model="message"></textarea>
    </div>
    <button type="submit" class="btn btn-primary">Submit</button>
    <button type="reset" class="btn btn-danger">Reset</button>
  </form>
</template>

<script>
import { store } from "../assets/data/store";
import axios from 'axios';
export default {
  name: 'ContactForm',
  data() {
    return {
      store,
      name: '',
      email: '',
      address: '',
      message: '',
    }
  },
  methods: {
    submitForm() {
      const data = {
        name: this.name,
        email: this.email,
        address: this.address,
        message: this.message
      }
      axios.post(this.store.apiUrl + 'contacts', data).then((res) => {
        console.log(res);
        this.name = '';
        this.email = '';
        this.address = '';
        this.message = '';
      }).catch((err) => {
        console.log('error', err);
      })
    }
  }
}
</script>

<style lang="scss" scoped></style>