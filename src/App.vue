<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';

export default{
  components: {
    AppHeader,
    AppMain,
    AppFooter
  }
}
</script>

<template>

  <header>
    <AppHeader />
  </header>

  <main>
    <AppMain />
  </main>

  <footer>
    <AppFooter />
  </footer>

</template>

<style>
  *{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    list-style-type: none;
  }
</style>
