<template>
  <div>
    <v-container pt-0>
      <v-layout row wrap>
        <v-flex xs12 md8 class="center">
          <v-flex md8 justify-center row class="left-side">
            <img src="https://agora.id/wp-content/uploads/2019/07/agora-logo-cropped@2x.png" alt />
            <b><p>Welcome, Please login to continue</p></b>
            <form>
              <v-text-field
                v-model="email"
                label="E-mail"
                required></v-text-field>
              <v-text-field
                v-model="password"
                type="password"
                label="Password"
                required></v-text-field>
              <v-btn @click="submit" class="bg-agora">LOGIN</v-btn>
            </form>
            <br>
            <p>Continue Login with</p>
            <p>Don’t have an account? Register</p>
            <p>Forgot Password</p>
          </v-flex>
        </v-flex>
        <v-flex xs12 md4 justify-end>
          <img src="https://steveweddingphoto.com/wp-content/uploads/2018/06/MG_8913.jpg" alt="" width="100%" height="700px">
        </v-flex>
      </v-layout>
    </v-container>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
 .bg-agora {
     background-color: #BB2C4B !important;
     color: white;
     font-family: 'Montserrat', sans-serif;
 }
 .center {
   text-align: center;
 }
 img {margin-bottom: 30px;}
 .left-side {margin-top: 150px;}
</style>
