<template>
<div>
  <form @submit.prevent="submitLoginForm(formData)">
    <h3>Login</h3>
    <label>username</label>
    <input v-model="formData.username" />
    <label>password</label>
    <input v-model="formData.password" />
    <button>Login</button>
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
        password: ''
      }
    }
  },
  methods: {
    ...mapActions(['submitLoginForm'])
  }
}
</script>
