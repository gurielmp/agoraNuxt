<template>
  <v-flex xs12 md8 class="center">
    <v-flex md8 justify-center row class="forget-left">
      <h1 class="forget-title">
        FORGOT
        <span class="col-agora">PASSWORD</span>
      </h1>
      <p class="col-agora">Don’t worry, please type your active email used for register</p>
      <form>
        <v-text-field
          v-model="email"
          :rules="emailRules"
          label="E-mail"
          placeholder="exmaple@agora.id"
          required
        ></v-text-field>
        <v-btn @click="submit" class="bg-agora">submit</v-btn>
      </form>
    </v-flex>
  </v-flex>
</template>

<script>
export default {
  data() {
    return {
      valid: false,
      email: "",
      emailRules: [
        v => !!v || "E-mail is required",
        v => /.+@.+/.test(v) || "E-mail must be valid"
      ]
    };
  }
};
</script>

<style>
h1,p,form {font-family: "Montserrat", sans-serif;}
.col-agora {color: #bb2c4b;}
.forget-title {padding: 150px 0 40px}
.forget-left {padding: 0 60px}
</style>
