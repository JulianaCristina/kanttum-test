<template>
  <v-app>

    <Toolbar/>
    <v-content>
      <Sidebar/>
      <PageHeader/>
      <HelloWorld/>
    </v-content>
  </v-app>
</template>

<script>
import HelloWorld from './components/HelloWorld';
import Toolbar from "./components/Toolbar/Toolbar";
import Sidebar from "./components/Sidebar/Sidebar";
import PageHeader from "./components/PageHeader/PageHeader";

export default {
  name: 'App',

  components: {
    HelloWorld,
    Toolbar,
    Sidebar,
    PageHeader
  },

  data: () => ({
    //
  }),
};
</script>
