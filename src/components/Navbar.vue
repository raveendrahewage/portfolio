<template>
  <nav class="navbar" id="navbar">
    <div class="max-width">
      <div class="logo">
        <a href="#">R<span>V.</span></a>
      </div>
      <ul class="menu" id="menu">
        <li><a href="#home" @click="menu" class="menu-btn">Home</a></li>
        <li><a href="#about" @click="menu" class="menu-btn">About</a></li>
        <li><a href="#skills" @click="menu" class="menu-btn">Skills</a></li>
        <li><a href="#projects" @click="menu" class="menu-btn">Projects</a></li>
        <li>
          <a href="#experience" @click="menu" class="menu-btn">Experience</a>
        </li>
        <li><a href="#contact" @click="menu" class="menu-btn">Contact</a></li>
      </ul>
      <div class="menu-btn" @click="menu">
        <i class="fas fa-bars" id="menu-icon"></i>
      </div>
    </div>
    <div class="scroll-up-btn" id="scroll-up-btn" @click="scrollTop">
      <i class="fas fa-angle-up"></i>
    </div>
  </nav>
</template>

<script>
export default {
  name: "Navbar",
  mounted() {
    setInterval(() => {
      this.sticky();
    }, 1);
  },
  methods: {
    menu() {
      document.getElementById("menu").classList.toggle("active");
      document.getElementById("menu-icon").classList.toggle("active");
    },
    sticky() {
      var navbar = document.getElementById("navbar");
      if (window.pageYOffset != 0) {
        navbar.classList.add("sticky");
      } else {
        navbar.classList.remove("sticky");
      }

      var scrollBtn = document.getElementById("scroll-up-btn");
      if (window.pageYOffset > 500) {
        scrollBtn.classList.add("show");
      } else {
        scrollBtn.classList.remove("show");
      }
    },

    scrollTop() {
      document.body.scrollTop = 0;
      document.documentElement.scrollTop = 0;
    },
  },
};
</script>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;700&family=Ubuntu:wght@400;500;700&display=swap");
@import url("https://pro.fontawesome.com/releases/v5.10.0/css/all.css");

* {
  box-sizing: border-box;
  text-decoration: none;
}

.max-width {
  max-width: 1300px;
  padding: 0 80px;
  margin: auto;
}

.scroll-up-btn {
  position: fixed;
  height: 45px;
  width: 42px;
  background: rgb(231, 93, 0);
  right: 30px;
  bottom: 10px;
  text-align: center;
  line-height: 45px;
  color: #fff;
  z-index: 9999;
  font-size: 30px;
  border-radius: 6px;
  border-bottom-width: 2px;
  cursor: pointer;
  opacity: 0;
  pointer-events: none;
  transition: all 0.3s ease;
}
.scroll-up-btn.show {
  bottom: 30px;
  opacity: 1;
  pointer-events: auto;
}
.scroll-up-btn:hover {
  filter: brightness(90%);
}

/* Navbar */
.navbar {
  position: fixed;
  width: 100%;
  z-index: 999;
  padding: 30px 0;
  background-color: tranparent;
  font-family: "Ubuntu", sans-serif;
  transition: all 0.3s ease;
}
.navbar.sticky {
  padding: 15px 0;
  background: rgb(231, 93, 0);
}
.navbar .max-width {
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.navbar .logo a {
  color: #fff;
  font-size: 35px;
  font-weight: 600;
}
.navbar .logo a span {
  color: rgb(231, 93, 0);
  transition: all 0.3s ease;
}
.navbar.sticky .logo a span {
  color: rgb(0, 0, 0);
}
.navbar .menu li {
  list-style: none;
  display: inline-block;
}
.navbar .menu li a {
  display: block;
  color: #fff;
  font-size: 18px;
  font-weight: 500;
  margin-left: 25px;
  transition: color 0.3s ease;
}
.navbar .menu li a:hover {
  color: rgb(231, 93, 0);
}
.navbar.sticky .menu li a:hover {
  color: rgb(0, 0, 0);
}

.menu-btn {
  color: #fff;
  font-size: 23px;
  cursor: pointer;
  display: none;
}

.menu-btn img {
  width: 20px;
}

@media (max-width: 947px) {
  .max-width {
    padding: 0 50px;
  }

  .menu-btn {
    display: block;
    z-index: 999;
  }
  .menu-btn i.active:before {
    content: "\f00d";
  }

  .navbar .menu {
    position: fixed;
    height: 100vh;
    width: 100%;
    left: -100%;
    top: 0;
    background: #111;
    text-align: center;
    padding-top: 80px;
    transition: all 0.3s ease;
  }
  .navbar .menu.active {
    left: 0;
  }
  .navbar .menu li {
    display: block;
  }
  .navbar .menu li a {
    display: inline-block;
    margin: 20px 0;
    font-size: 25px;
  }
}

@media (max-width: 500px) {
  .scroll-up-btn {
    right: 15px;
    bottom: 15px;
    height: 38px;
    width: 35px;
    font-size: 23px;
    line-height: 38px;
  }
}
</style>
