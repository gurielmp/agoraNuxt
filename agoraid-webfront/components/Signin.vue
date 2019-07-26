<template>
  <v-flex xs12 md8 class="center">
    <v-flex md8 justify-center row class="left-side">
      <img src="https://agora.id/wp-content/uploads/2019/07/agora-logo-cropped@2x.png" alt />
      <b>
        <p>Welcome, Please login to continue</p>
      </b>
      <form>
        <v-text-field v-model="email" label="E-mail" required></v-text-field>
        <v-text-field v-model="password" type="password" label="Password" required></v-text-field>
        <v-btn @click="submit" class="bg-agora">LOGIN</v-btn>
      </form>
      <br />
      <p>Continue Login with</p>
      <p>
        Don’t have an account?
        <nuxt-link to="/sign-up">Register</nuxt-link>
      </p>
      <p>
        <nuxt-link to="forget-password">Forgot Password</nuxt-link>
      </p>
    </v-flex>
  </v-flex>
</template>

<script>
export default {};
</script>

<style>
.bg-agora {
  background-color: #bb2c4b !important;
  color: white !important;
  font-family: "Montserrat", sans-serif;
}
p {font-family: "Montserrat", sans-serif;}
.left-side {margin-top: 50px;}
</style>
