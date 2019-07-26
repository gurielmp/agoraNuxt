<template>
  <div>
    <v-container pt-0>
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
 
</style>
