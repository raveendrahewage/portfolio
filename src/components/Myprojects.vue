<template>
  <section class="projects" id="projects">
    <div class="max-width">
      <h2 class="title">My Projects</h2>
      <div class="carousel">
        <div class="slideshow-container">
          <div
            class="hide card fade"
            @mouseover="walkietalkieImage = walkietalkieImage2"
            @mouseout="walkietalkieImage = walkietalkieImage1"
            @click="goToWalkieTalkie"
          >
            <div class="box">
              <img :src="walkietalkieImage" />
              <div class="text">Walkie-Talkie</div>
              <p>
                Walkie-Talkie is another chat application developed with Vue.js
                and deployed on firebase. Firebase firestore has been used as
                the databes and this facilitase the user to create chat rooms
                and send voice messages.
              </p>
            </div>
          </div>
          <div
            class="hide card fade"
            @mouseover="notesparkImage = notesparkImage2"
            @mouseout="notesparkImage = notesparkImage1"
            @click="goToNotesparkRepo"
          >
            <div class="box">
              <img :src="notesparkImage" />
              <div class="text">NotesPark</div>
              <p>
                NotesPark is a web application that facilitae the users to keep
                their notes and MEVN stack were used. This is also developed
                with Vue.js and vuetify plugin has been used. Mongodb databse
                has been used to store the user details and notes.
              </p>
            </div>
          </div>
          <div
            class="hide card fade"
            @mouseover="chitchatImage = chitchatImage2"
            @mouseout="chitchatImage = chitchatImage1"
            @click="goToChitChat"
          >
            <div class="box">
              <img :src="chitchatImage" />
              <div class="text">ChitChat</div>
              <p>
                ChitChat is a very simple chat aplication that allows you to
                chat with someone. This was also developed with Vue.js and I
                have user Firebase realtime database and deployment has also
                been done on Firebase.
              </p>
            </div>
          </div>
          <div
            class="hide card fade"
            @mouseover="careuImage = careuImage2"
            @mouseout="careuImage = careuImage1"
            @click="goToCareuRepo"
          >
            <div class="box">
              <img :src="careuImage" class="careu" />
              <div class="text">CareU</div>
              <p>
                CareU is a web application developed as a university project.
                The purpose of developing this application was to connect the
                people who are in the need of help of emergency services to
                those relevant services. As well as, any framework has not been
                used for this application. HTML, CSS , JavaScript and Jquery
                were used for this application.
              </p>
            </div>
          </div>
          <div
            class="hide card fade"
            @mouseover="skyreadsImage = skyreadsImage2"
            @mouseout="skyreadsImage = skyreadsImage1"
            @click="goToSkyreads"
          >
            <div class="box">
              <img :src="skyreadsImage" />
              <div class="text">Skyreads</div>
              <p>
                Skyreads is web application where yu can check the wheather of
                any place in the world. In this application, you can search any
                palce and get the details like rain status, humadity, wind speed
                and etc. I have user Vue.js, Axios and Bootstrap for developing
                this application.This has been deployed on Bytehost.
              </p>
            </div>
          </div>
          <div
            class="hide card fade"
            @mouseover="friendtodoImage = friendtodoImage2"
            @mouseout="friendtodoImage = friendtodoImage1"
            @click="goToFriendtToDo"
          >
            <div class="box">
              <img :src="friendtodoImage" />
              <div class="text">FriendToDo</div>
              <p>
                FriendToDo is a simple web application where you can list out
                your works to be done in the future. Node.js, EJS{Embaded
                Javascript Templating) Express and Jquery and Mongoose database
                has been used to develop this appilicaton. This has been
                deployed on Heroku.
              </p>
            </div>
          </div>
          <div class="hide card fade" @click="goToFacememo">
            <div class="box">
              <img :src="facememoImage" class="facememo" />
              <div class="text">FaceMemo</div>
              <p>
                FaceMemo is a small game that has been created using javascript,
                HTML and Bootstrap only. This has been deployed on github pages.
              </p>
            </div>
          </div>
          <a class="prev" @click="plusSlides(-1)">&#10094;</a>
          <a class="next" @click="plusSlides(1)">&#10095;</a>
          <div class="dots" style="text-align:center">
            <span class="dot" @click="currentSlide(1)"></span>
            <span class="dot" @click="currentSlide(2)"></span>
            <span class="dot" @click="currentSlide(3)"></span>
            <span class="dot" @click="currentSlide(4)"></span>
            <span class="dot" @click="currentSlide(5)"></span>
            <span class="dot" @click="currentSlide(6)"></span>
            <span class="dot" @click="currentSlide(7)"></span>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Myprojects",
  data() {
    return {
      slideIndex: 1,
      facememoImage: require("./../assets/facememo/1.png"),
      facememoImage1: require("./../assets/facememo/1.png"),
      facememoImage2: require("./../assets/facememo/2.png"),
      friendtodoImage: require("./../assets/friendtodo/1.png"),
      friendtodoImage1: require("./../assets/friendtodo/1.png"),
      friendtodoImage2: require("./../assets/friendtodo/2.png"),
      careuImage: require("./../assets/careu/1.png"),
      careuImage1: require("./../assets/careu/1.png"),
      careuImage2: require("./../assets/careu/2.png"),
      skyreadsImage: require("./../assets/skyreads/1.png"),
      skyreadsImage1: require("./../assets/skyreads/1.png"),
      skyreadsImage2: require("./../assets/skyreads/2.png"),
      chitchatImage: require("./../assets/chitchat/1.png"),
      chitchatImage1: require("./../assets/chitchat/1.png"),
      chitchatImage2: require("./../assets/chitchat/2.png"),
      notesparkImage: require("./../assets/notespark/1.png"),
      notesparkImage1: require("./../assets/notespark/1.png"),
      notesparkImage2: require("./../assets/notespark/2.png"),
      walkietalkieImage: require("./../assets/walkietalkie/1.png"),
      walkietalkieImage1: require("./../assets/walkietalkie/1.png"),
      walkietalkieImage2: require("./../assets/walkietalkie/2.png"),
    };
  },
  mounted() {
    this.showSlides(this.slideIndex);
  },
  methods: {
    plusSlides(n) {
      this.showSlides((this.slideIndex += n));
    },

    currentSlide(n) {
      this.showSlides((this.slideIndex = n));
    },

    showSlides(n) {
      var i;
      var slides = document.getElementsByClassName("hide card");
      var dots = document.getElementsByClassName("dot");
      if (n > slides.length) {
        this.slideIndex = 1;
      }
      if (n < 1) {
        this.slideIndex = slides.length;
      }
      for (i = 0; i < slides.length; i++) {
        slides[i].style.display = "none";
      }
      for (i = 0; i < dots.length; i++) {
        dots[i].className = dots[i].className.replace(" active", "");
      }
      slides[this.slideIndex - 1].style.display = "block";
      dots[this.slideIndex - 1].className += " active";
    },

    goToFacememo() {
      window.open("https://raveendrahewage.github.io/facememo/", "_blank");
    },

    goToFriendtToDo() {
      window.open("https://friendtodo.herokuapp.com/", "_blank");
    },

    goToCareuRepo() {
      window.open("https://github.com/raveendrahewage/CAREU_WEB", "_blank");
    },

    goToSkyreads() {
      window.open("http://skyreads.byethost11.com/", "_blank");
    },

    goToChitChat() {
      window.open("https://chitchat-a63f5.web.app/", "_blank");
    },
    goToNotesparkRepo() {
      window.open("https://github.com/raveendrahewage/notespark", "_blank");
    },
    goToWalkieTalkie() {
      window.open("https://walki-talkie-1729a.web.app/#/", "_blank");
    },
  },
};
</script>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;700&family=Ubuntu:wght@400;500;700&display=swap");
/* @import url('https://cdnjs.cloudflare.com/ajax/libs/OwlCarousel2/2.3.4/assets/owl.carousel.min.css'); */

* {
  box-sizing: border-box;
  text-decoration: none;
}

section {
  padding: 50px 0;
  position: relative;
}

.slideshow-container {
  max-width: 1000px;
  position: relative;
  margin: auto;
}

.dot {
  cursor: pointer;
  height: 15px;
  width: 15px;
  margin: 0 5px;
  background-color: #bbb;
  border-radius: 50%;
  display: inline-block;
  transition: background-color 0.6s ease;
}

.dots {
  margin: 0.5rem;
}

.prev,
.next {
  cursor: pointer;
  position: absolute;
  top: 37%;
  width: auto;
  padding: 16px;
  margin-top: -22px;
  color: white;
  font-weight: bold;
  font-size: 50px;
  transition: 0.6s ease;
  border-radius: 0 3px 3px 0;
  user-select: none;
}

.prev {
  left: -60px;
}

.next {
  right: -60px;
  border-radius: 3px 0 0 3px;
}

.prev:hover,
.next:hover {
  color: rgb(231, 93, 0);
}

.active,
.dot:hover {
  background-color: rgb(231, 93, 0);
}

.fade {
  -webkit-animation-name: fade;
  -webkit-animation-duration: 1.5s;
  animation-name: fade;
  animation-duration: 1.5s;
}

@-webkit-keyframes fade {
  from {
    opacity: 0.2;
  }
  to {
    opacity: 1;
  }
}

@keyframes fade {
  from {
    opacity: 0.2;
  }
  to {
    opacity: 1;
  }
}

.hide {
  display: none;
}

.max-width {
  max-width: 1300px;
  padding: 0 80px;
  margin: auto;
}

.projects {
  color: #fff;
  background: #111;
  font-family: "Poppins", sans-serif;
}

.title {
  position: relative;
  text-align: center;
  font-size: 40px;
  font-weight: 500;
  margin-bottom: 60px;
  padding-bottom: 20px;
  font-family: "Ubuntu", sans-serif;
}

.projects .title::before {
  background: #fff;
}

.projects .title::after {
  background: #111;
  content: "what i provide";
}

.title::before {
  content: "";
  position: absolute;
  bottom: 0px;
  left: 50%;
  width: 180px;
  height: 3px;
  background: #111;
  transform: translateX(-50%);
}

.title::after {
  position: absolute;
  bottom: -8px;
  left: 50%;
  font-size: 20px;
  color: rgb(231, 93, 0);
  padding: 0 5px;
  background: #fff;
  transform: translateX(-50%);
}

.projects .title::after {
  content: "what i have done";
}
.projects .carousel .card {
  background: #222;
  border-radius: 6px;
  padding: 25px 35px;
  text-align: center;
  overflow: hidden;
  transition: all 0.3s ease;
}
.projects .carousel .card:hover {
  background: rgb(231, 93, 0);
}
.projects .carousel .card .box {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  cursor: pointer;
  transition: all 0.3s ease;
}
.projects .carousel .card:hover .box {
  transform: scale(1.05);
}
.projects .carousel .card .text {
  font-size: 25px;
  font-weight: 500;
  margin: 10px 0 7px 0;
}
.projects .carousel .card img {
  height: auto;
  width: 100%;
  object-fit: cover;
  border: 5px solid rgb(231, 93, 0);
  transition: all 0.3s ease;
}

.projects .carousel .card .facememo:hover {
  content: url("./../assets/facememo/2.png");
}

.projects .carousel .card:hover img {
  transition: all 0.3s linear;
  border-color: #fff;
}
.owl-dots {
  text-align: center;
  margin-top: 20px;
}
.owl-dot {
  height: 13px;
  width: 13px;
  margin: 0 5px;
  outline: none !important;
  border-radius: 50%;
  border: 2px solid rgb(231, 93, 0) !important;
  transition: all 0.3s ease;
}
.owl-dot.active {
  width: 35px;
  border-radius: 14px;
}
.owl-dot.active,
.owl-dot:hover {
  background: rgb(231, 93, 0) !important;
}

@media (max-width: 947px) {
  .max-width {
    max-width: 930px;
  }
}

@media (max-width: 690px) {
  .max-width {
    padding: 0 23px;
  }

  .prev {
    left: 0;
  }

  .next {
    right: 0;
  }
}
</style>
