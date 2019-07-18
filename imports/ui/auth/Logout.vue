<template>
<button @click="logout">Logout</button>
</template>

<script>
  import { mapActions } from 'vuex';
export default {
  methods: {
    ...mapActions(['logout'])
  }
}
</script>
