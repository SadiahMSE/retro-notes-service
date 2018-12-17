<template>
  <div id="app">
    <Header/>
   <div id="nav">
      <router-link to="/">Notes</router-link> |
      <router-link to="/about">Enter notes</router-link>
    </div>
    <router-view/> 
    <NoteEntry/>

    <!-- <HelloWorld/> -->
    <Footer2/>
  </div>
  
</template>

<script>
  import Header from './components/Header.vue';
  import NoteEntry from './components/NoteEntry.vue';
  import Footer2 from './components/Footer2.vue';
  // import HelloWorld from './components/HelloWorld.vue';

  export default {
    name: 'App',
    components: {
      Header,
      NoteEntry,
      Footer2
    }
}

</script>

<style>
  #app,body,html {
    margin: 0px;
    padding: 0px;
  }
</style>
