<template>
  <div class="introduction-page">
    <SignIn v-on:signIn="signInUser()"/>
  </div>
</template>
<script lang="ts">
import SignIn from '@/components/SignIn.vue';
export default {
  components: {
    SignIn
  },
  methods: {
    signInUser() {
      this.$forceUpdate();
      localStorage.setItem('introDone', "true");
      this.$router.push('/sign-in');
    }
  }
}
</script>
<style scoped>
.introduction-page {
    padding-top: 14vh;
    padding-bottom:80px;
}
</style>