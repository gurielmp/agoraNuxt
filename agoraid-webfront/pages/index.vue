<template>
  <div>
    <v-container pa-0 class="bg-white">
      <v-layout row wrap>
        <Signin/>
        <Formbg/>
      </v-layout>
    </v-container>
  </div>
</template>

<script>
import Signin from '~/components/Signin.vue';
import Formbg from '~/components/Formbg.vue';
export default {
  components: {
    Signin,
    Formbg
  }
};
</script>

<style>
 .center {
   text-align: center;
 }
 .bg-white {background-color: white;}
</style>
