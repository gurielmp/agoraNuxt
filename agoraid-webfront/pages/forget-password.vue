<template>
  <div>
    <v-container>
      <v-layout row wrap>
        <v-flex xs12 md8 class="center">
            <v-flex md6 justify-center row>
                <h1>forgot password</h1>
                <p class="c-agora">Don’t worry, please type your active email used for register</p>
                <form>
                <v-text-field
                v-model="email"
                label="E-mail"
                required
                ></v-text-field>
                <v-btn @click="submit" class="bg-agora">submit</v-btn>
                </form>
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

<style scoped>
    .bg-agora {
        background-color: #BB2C4B !important;
        color: white;
        font-family: 'Montserrat', sans-serif;
    }
    .c-agora {
        color: #BB2C4B;
    }
    h1 {
        text-transform: uppercase;
    }
    .center {text-align: center;}
</style>
