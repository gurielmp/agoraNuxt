<template>
  <div>
    <v-container pa-0 class="bg-white">
      <v-layout row wrap>
        <Signup/>
        <Formbg/>
      </v-layout>
    </v-container>
  </div>
</template>

<script>
import Signup from '~/components/Signup.vue';
import Formbg from '~/components/Formbg.vue';
export default {
  components: {
    Signup,
    Formbg
  }
};
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
