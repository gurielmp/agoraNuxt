<template>
  <div>
    <v-container>
      <v-layout row wrap>
        <v-flex xs12 md8 class="center">
            <v-flex md8 justify-center row>
                <h1>Create an account</h1>
                <p justify-center>You’ll need an account to get to your courses</p>
                <form>
                <v-text-field
                v-model="email"
                label="E-mail"
                required
                ></v-text-field>
                <v-text-field
                v-model="password"
                type="password"
                label="Password"
                required
                ></v-text-field>
                <v-text-field
                v-model="password"
                type="password"
                label="Confirm Password"
                required
                ></v-text-field>
                <v-btn @click="submit" class="bg-agora">Register</v-btn>
            </form>
            <p>or Register with</p>
            (spot logo)
            <p>Already have account? Login</p>
          </v-flex>
        </v-flex>
        <v-flex xs12 md4>
            <img src="https://steveweddingphoto.com/wp-content/uploads/2018/06/MG_8913.jpg" alt="">
        </v-flex>
      </v-layout>
    </v-container>
  </div>
</template>

<script>
export default {};
</script>
<style>
    .bg-agora {
        background-color: #BB2C4B !important;
        color: white !important;
        font-family: 'Montserrat', sans-serif;
    }
    h1,p {
        font-family: 'Montserrat', sans-serif;
    }
    h1 {
        text-transform: uppercase;
    }
    .center {
        text-align: center;
    }
</style>
