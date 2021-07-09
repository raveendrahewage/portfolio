<template>
  <section class="home" id="home">
    <div class="max-width">
      <div class="home-content">
        <div class="text-1">Hello, my name is</div>
        <div class="text-2">Raveendra Hewage</div>
        <div class="text-3">And I'm <span class="typing"></span></div>
      </div>
    </div>
  </section>
</template>

<script>
import Typed from "typed.js";
export default {
  name: "Home",
  data() {
    return {
      options: {
        strings: ["a Developer", "a Programmar", "an Undergraduate"],
        typeSpeed: 40,
        backSpeed: 60,
        loop: true,
      },
    };
  },
  mounted() {
    var typed = new Typed(".typing", this.options);
  },
};
</script>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;700&family=Ubuntu:wght@400;500;700&display=swap");

* {
  box-sizing: border-box;
  text-decoration: none;
}

section {
  padding: 50px 0;
}

.max-width {
  max-width: 1300px;
  padding: 0 80px;
  margin: auto;
}
/* Home */
.home {
  display: flex;
  height: 100vh;
  color: #fff;
  min-height: 500px;
  background-image: url("./../assets/banner.jpg");
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  font-family: "Ubuntu", sans-serif;
}

.home .max-width {
  margin: auto 0 auto 40px;
}

.home .home-content .text-1 {
  font-size: 27px;
}

.home .home-content .text-2 {
  font-size: 75px;
  font-weight: 600;
  margin-left: -3px;
}

.home .home-content .text-3 {
  font-size: 27px;
  margin: 5px 0;
}

.home .home-content .text-3 span {
  color: rgb(231, 93, 0);
  font-weight: 500;
}

@media (max-width: 1300px) {
  .home .max-width {
    margin-left: 0px;
  }
}

@media (max-width: 947px) {
  .max-width {
    max-width: 930px;
  }
  .home .home-content .text-2 {
    font-size: 70px;
  }
  .home .home-content .text-3 {
    font-size: 35px;
  }
  .home .home-content a {
    font-size: 23px;
    padding: 10px 30px;
  }
}

@media (max-width: 690px) {
  .max-width {
    padding: 0 23px;
  }
  .home .home-content .text-2 {
    font-size: 60px;
  }
  .home .home-content .text-3 {
    font-size: 32px;
  }
  .home .home-content a {
    font-size: 20px;
  }
}

@media (max-width: 500px) {
  .home .home-content .text-2 {
    font-size: 50px;
  }
  .home .home-content .text-3 {
    font-size: 27px;
  }
}
</style>
