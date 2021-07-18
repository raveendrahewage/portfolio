<template>
  <section class="about" id="about">
    <div class="max-width">
      <h2 class="title">About me</h2>
      <div class="about-content">
        <div class="column left">
          <img src="./../assets/my1.jpg" alt="" />
        </div>
        <div class="column right">
          <div class="text">
            I'm Raveendra and I'm a <span class="typing-2"></span>
          </div>
          <p>
            I am a very simple person who works hard for reaching to success and
            has a passion for learning new things. Currently, I am a third-year
            undergraduate at the University of Colombo School of Computing and
            do the B.Sc in Computer Science degree there. WP/MT Yattapatha K.V
            was my school up until my O/L and I did my A/L from Ananda
            Sastralaya, Matugama. I am very interested in web development and
            work on it by learning new technologies and brushing up my skills.
            My ambition also to starts my career in that field. Most of the
            time, I spend my free time listening to music and writing poems. It
            gives me a lot of relaxation and refreshments to my day-to-day life.
            As well, I do video editing as one of my hobbies too.
          </p>
          <a :href="cvLink" download="RaveendraHewage">Download CV</a>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import Typed from "typed.js";
export default {
  name: "About",
  data() {
    return {
      options: {
        strings: [
          "undergraduate.",
          "simple person.",
          "hard worker.",
          "music lover.",
          "fast learner.",
        ],
        typeSpeed: 40,
        backSpeed: 60,
        loop: true,
      },
      cvLink: require("./../assets/CV/cv.png"),
    };
  },
  mounted() {
    var typed = new Typed(".typing-2", this.options);
  },
};
</script>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;700&family=Ubuntu:wght@400;500;700&display=swap");

* {
  box-sizing: border-box;
  text-decoration: none;
}

.max-width {
  max-width: 1300px;
  padding: 0 80px;
  margin: auto;
}

/* About */
section {
  padding: 50px 0;
}

.typing {
  color: rgb(231, 93, 0);
}

.about {
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

.about .about-content {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  justify-content: space-between;
}

.about .title::after {
  content: "who i am";
}
.about .about-content .left {
  width: 45%;
}
.about .about-content .left img {
  height: 400px;
  width: 400px;
  object-fit: cover;
  border-radius: 6px;
}
.about .about-content .right {
  width: 55%;
}
.about .about-content .right .text {
  font-size: 25px;
  font-weight: 600;
  margin-bottom: 10px;
}
.about .about-content .right .text span {
  color: rgb(231, 93, 0);
}
.about .about-content .right p {
  text-align: justify;
}
.about .about-content .right a {
  display: inline-block;
  background: rgb(231, 93, 0);
  color: #fff;
  font-size: 20px;
  font-weight: 500;
  padding: 10px 30px;
  margin-top: 20px;
  border-radius: 6px;
  border: 2px solid rgb(231, 93, 0);
  transition: all 0.3s ease;
}
.about .about-content .right a:hover {
  color: rgb(231, 93, 0);
  background: none;
}

@media (max-width: 1104px) {
  .about .about-content .left img {
    height: 350px;
    width: 350px;
  }
}

@media (max-width: 947px) {
  .max-width {
    max-width: 930px;
  }
  .about .about-content .column {
    width: 100%;
  }
  .about .about-content .left {
    display: flex;
    justify-content: center;
    margin: 0 auto 60px;
  }
  .about .about-content .right {
    flex: 100%;
  }
}

@media (max-width: 500px) {
  .about .about-content .right .text {
    font-size: 19px;
  }
}
</style>
