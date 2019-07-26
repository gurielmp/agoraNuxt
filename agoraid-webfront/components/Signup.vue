<template>
  <v-flex xs12 md8 class="center">
    <v-flex md8 justify-center row left-side>
      <h1 class="signup-title">Create an account</h1>
      <p justify-center class="signup-p">You’ll need an account to get to your courses</p>
      <form>
        <v-text-field v-model="email" :rules="emailRules" label="E-mail" 
        placeholder="exmaple@agora.id" required></v-text-field>
        <v-text-field class="montserrat"
            :append-icon="show3 ? 'visibility' : 'visibility_off'"
            :rules="[rules.required, rules.min]"
            :type="show3 ? 'text' : 'password'"
            name="input-10-2"
            label="Password"
            hint="At least 8 characters"
            value=""
            placeholder="********"
            @click:append="show3 = !show3"
          ></v-text-field>
        <v-text-field
            :append-icon="show3 ? 'visibility' : 'visibility_off'"
            :rules="[rules.required, rules.min]"
            :type="show3 ? 'text' : 'password'"
            name="input-10-2"
            label="Confirm Password"
            hint="At least 8 characters"
            value=""
            placeholder="********"
            @click:append="show3 = !show3"
          ></v-text-field>
        <v-btn @click="submit" class="bg-agora">Register</v-btn>
      </form>
      <br>
      <p>Or Register with</p>
    <div>
        <img src="~/assets/images/google-plus.png" alt="" class="img-margin">
        <img src="~/assets/images/linkedin.png" alt="" class="img-margin">
    </div>
      <p>
        Already have account?
        <nuxt-link to="/" class="col-agora">Login</nuxt-link>
      </p>
    </v-flex>
  </v-flex>
</template>

<script>
export default {
    data () {
      return {
        valid: false,
        email: '',
        emailRules: [
            v => !!v || 'E-mail is required',
            v => /.+@.+/.test(v) || 'E-mail must be valid',
        ],    
        show3: false,
        password: 'Password',
        rules: {
          required: value => !!value || 'Required.',
          min: v => v.length >= 8 || 'Min 8 characters',
          emailMatch: () => ('The email and password you entered don\'t match'),
        },
      }
    },
  }
</script>

<style>
    .signup-title {padding-top: 30px;}
    .signup-p {padding: 5px 0 30px 0}
    .montserrat {font-family: "Montserrat", sans-serif;}
</style>
