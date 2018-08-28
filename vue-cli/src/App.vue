<template>
  <div id="app">
    <Header/>
    <NoteEntry/>
  </div>
</template>

<script>
  import Header from './components/Header.vue';
  import NoteEntry from './components/NoteEntry.vue';

  export default {
    name: 'App',
    components: {
      Header,
      NoteEntry
    }
}

</script>

<style>
  #app,body,html {
    margin: 0px;
    padding: 0px;
  }
</style>
