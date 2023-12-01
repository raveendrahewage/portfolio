<template>
  <div id="app">
    <Navbar />
    <Home />
    <About />
    <!-- <Myprojects /> -->
    <Experience />
    <Skills />
    <Contact />
    <Footer />
    <particles-bg color="black" type="square" :num="10" :bg="true" />
  </div>
</template>

<script>
import Navbar from "./components/Navbar";
import Home from "./components/Home";
import About from "./components/About";
// import Myprojects from "./components/Myprojects";
import Experience from "./components/Experience";
import Skills from "./components/Skills";
import Contact from "./components/Contact";
import Footer from "./components/Footer";
import { ParticlesBg } from "particles-bg-vue";

export default {
  name: "App",
  components: {
    Navbar,
    Home,
    About,
    // Myprojects,
    Experience,
    Skills,
    Contact,
    Footer,
    ParticlesBg,
  },
};
</script>

<style>
* {
  box-sizing: border-box;
  text-decoration: none;
}

html {
  scroll-behavior: smooth;
}

body {
  margin: 0;
}

body::-webkit-scrollbar-track {
  -webkit-box-shadow: inset 0 0 6px rgba(0, 0, 0, 0.3);
  border-radius: 10px;
  background-color: rgb(0, 0, 0);
}

body::-webkit-scrollbar {
  width: 12px;
  background-color: rgb(0, 0, 0);
}

body::-webkit-scrollbar-thumb {
  border-radius: 10px;
  -webkit-box-shadow: inset 0 0 6px rgb(102, 46, 0);
  background-color: rgb(129, 52, 0);
}
</style>
