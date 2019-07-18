<template>
<div>
  <form @submit.prevent="submitRegisterForm(formData)">
    <h3>Register</h3>
    <label>username</label>
    <input v-model="formData.username"/>
    <label>email</label>
    <input v-model="formData.email"/>
    <label>password</label>
    <input v-model="formData.password" />
    <button>Register</button>
  </form>
</div>
</template>

<script>
  import { mapActions } from 'vuex';
export default {
  data() {
    return {
      formData: {
        username: '',
        email: '',
        password: ''
      }
    }
  },
  methods: {
    ...mapActions(['submitRegisterForm'])
  }
}
</script>
