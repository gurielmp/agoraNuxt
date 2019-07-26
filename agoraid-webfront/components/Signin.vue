<template>
  <v-flex xs12 md8 container-space class="center">
    <v-flex md8 justify-center row class="left-side">
      <img class="img-logo" src="~/assets/images/agora-logo-cropped.png" alt />
        <p class="welcome-style">Welcome, Please login to continue</p>
      <form>
        <v-text-field v-model="email" :rules="emailRules" label="E-mail" 
        placeholder="exmaple@agora.id" required></v-text-field>
        <v-text-field
            :append-icon="show3 ? 'visibility' : 'visibility_off'"
            :type="show3 ? 'text' : 'password'"
            name="input-10-2"
            label="Password"
            placeholder="********"
            class="input-group--focused"
            @click:append="show3 = !show3"
          ></v-text-field>
        <v-btn @click="submit" class="bg-agora">LOGIN</v-btn>
      </form>
      <br/>
      <p>Continue Login With</p>
      <v-flex md12>
        <img src="~/assets/images/google-plus.png" alt="" class="img-margin">
        <img src="~/assets/images/linkedin.png" alt="" class="img-margin">
      </v-flex>
      <p>
        Don’t have an account?
        <nuxt-link to="/sign-up" class="col-agora">Register</nuxt-link>
      </p>
      <p>
        <nuxt-link to="forget-password" class="col-forgot">Forgot Password</nuxt-link>
      </p>
    </v-flex>
  </v-flex>
</template>

<script>
export default {
    data: () => ({
      valid: false,
      email: '',
      emailRules: [
        v => !!v || 'E-mail is required',
        v => /.+@.+/.test(v) || 'E-mail must be valid',
      ],
      show3: false,
      password: 'Password',
    }),
  }
</script>

<style>
h1,p,form {font-family: "Montserrat", sans-serif;}
.bg-agora {
  background-color: #bb2c4b !important;
  color: white !important;
  font-family: "Montserrat", sans-serif;
  width: 110px;
}
.left-side {margin-top: 50px; padding: 0 80px;}
.img-logo {margin: 60px 0 30px;}
.col-agora {color: #bb2c4b;}
.col-forgot {color: #B4B4C9;}
.img-margin {margin: 5px 5px 40px 5px;}
.container-space {padding-bottom: 40px;}
.welcome-style {padding: 10px 0 30px;}
</style>
