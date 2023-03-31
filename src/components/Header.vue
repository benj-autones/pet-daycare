<template>
  <q-header elevated class="bg-primary text-white">
    <q-toolbar>
      <q-btn dense flat round icon="menu" @click="drawer = !drawer" />

      <q-toolbar-title class="q-mx-md">{{ title }}</q-toolbar-title>

      <q-btn dense flat round icon="notifications" />

      <q-btn dense flat round icon="settings" />
    </q-toolbar>
  </q-header>
</template>

<script>
export default {
  name: 'Header',
  props: {
    title: {
      type: String,
      default: 'Pet Daycare',
    },
  },
  data() {
    return {
      drawer: false,
    };
  },
};
</script>
