<template>
  <div>
    <v-container pa-0>
      <v-layout row wrap>
        <Forget/>
        <Formbg/>
      </v-layout>
    </v-container>
  </div>
</template>

<script>
import Forget from '~/components/Forget.vue';
import Formbg from '~/components/Formbg.vue';
export default {
  components: {
    Forget,
    Formbg
  }
};
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
