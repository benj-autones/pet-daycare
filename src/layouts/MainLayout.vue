<template>
  <q-layout>
    <Header />
    <Home />
  </q-layout>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import Header from 'components/Header.vue';
import Home from 'components/Home.vue';

export default defineComponent({
  name: 'MainLayout',

  components: {
    Header,
    Home,
  },
});
</script>
