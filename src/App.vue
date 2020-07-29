<template>
  <v-app id="app">
      <AppNavBar/>
      <AppLoading/>
      <AppContent/>
  </v-app>
</template>

<script>
import AppNavBar from './components/AppNavBar'
import AppContent from './components/AppContent'
import AppLoading from './components/AppLoading'

export default {
  name: 'App',
  data: () => ({
    //
  }),
  components: {
    AppNavBar,
    AppContent,
    AppLoading,
  }
};
</script>
<style>
  .box {
    width: 100%;
    margin-right: auto;
    margin-left: auto;
    padding-right: 1.5rem;
    padding-left: 1.5rem
  }

  @media (min-width:640px) {
    .box {
      max-width: 640px
    }
  }

  @media (min-width:768px) {
    .box {
      max-width: 768px
    }
  }

  @media (min-width:992px) {
    .box {
      max-width: 992px
    }
  }
</style>