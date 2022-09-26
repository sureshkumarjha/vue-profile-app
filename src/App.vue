<template>
  <NavBar />
    <router-link to="/">Home</router-link> |
    <!-- <router-link to="/about">About</router-link> -->
  <router-view />
  <FooterComponent/>
</template>

<script>
import NavBar from "./components/NavBar.vue";
import FooterComponent from './components/FooterComponent.vue';
import 'tachyons';
import './App.css';

export default {
  components: {
    NavBar,
    FooterComponent
},
};
</script>
