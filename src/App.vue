<template>
  <Navbar/>
  <Home/>
  <About/>
  <Myprojects/>
  <Skills/>
  <Contact/>
  <Footer/>
  <Contactform/>
</template>

<script>

import Navbar from './components/Navbar';
import Home from './components/Home';
import About from './components/About';
import Myprojects from './components/Myprojects';
import Skills from './components/Skills';
import Contact from './components/Contact';
import Footer from './components/Footer';
import Contactform from './components/Contactform';

export default {
  name: 'App',
  components: {
    Navbar,
    Home,
    About,
    Myprojects,
    Skills,
    Contact,
    Footer,
    Contactform
  }
}
</script>

<style>
*{
  box-sizing: border-box;
  text-decoration: none;
}

html{
    scroll-behavior: smooth;
}

body{
  margin:0;
}
</style>
