<template>
  <section class="skills" id="skills">
    <div class="max-width">
      <h2 class="title">Skills</h2>
      <div class="skills-content">
        <div class="column left">
          <div class="text">Languages Exposed</div>
          <div class="btn-group" style="width:100%">
            <button>PHP</button>
            <button>HTML</button>
            <button>JavaScript</button>
            <button>Python</button>
            <button>Scala</button>
            <button>R</button>
            <button>C</button>
            <button>C++</button>
          </div>
        </div>
        <div class="column right">
          <div class="text">Technologies Exposed</div>
          <div class="btn-group" style="width:100%">
            <button>Bootsrap</button>
            <button>Jquery</button>
            <button>Node JS</button>
            <button>.NET</button>
            <button>MySQL</button>
            <button>Angular</button>
            <button>Git</button>
            <button>Vue</button>
            <button>React</button>
            <button>React Native</button>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Skills",
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

.btn-group button {
  color: white;
  padding: 10px 24px;
  cursor: pointer;
  float: left;
  margin: 5px 5px 5px 0px;
  font-size: 20px;
  border-radius: 25px;
  background-color: #222;
  border: 1px solid #222;
  font-family: "Poppins", sans-serif;
}

.btn-group:after {
  content: "";
  clear: both;
  display: table;
}

.btn-group button:not(:last-child) {
  border-right: none;
}

.btn-group button:hover {
  background-color: rgb(206, 82, 0);
}

.max-width {
  max-width: 1300px;
  padding: 0 80px;
  margin: auto;
}

.skills {
  font-family: "Poppins", sans-serif;
}

.skills .skills-content {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  justify-content: space-between;
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
  background: rgb(0, 0, 0);
  transform: translateX(-50%);
}

.title::after {
  position: absolute;
  bottom: -8px;
  left: 50%;
  font-size: 20px;
  color: rgb(231, 93, 0);
  padding: 0 5px;
  background: rgb(255, 255, 255);
  transform: translateX(-50%);
}

.skills .title::after {
  content: "what i know";
  white-space: nowrap;
}

.skills .skills-content .column {
  width: calc(50% - 30px);
}

.skills .skills-content .left .text,
.skills .skills-content .right .text {
  font-size: 20px;
  font-weight: 600;
  margin-bottom: 10px;
}

.skills .skills-content .left p {
  text-align: justify;
}

.skills .skills-content .left a {
  display: inline-block;
  background: rgb(231, 93, 0);
  color: #fff;
  font-size: 18px;
  font-weight: 500;
  padding: 8px 16px;
  margin-top: 20px;
  border-radius: 6px;
  border: 2px solid rgb(231, 93, 0);
  transition: all 0.3s ease;
}

.skills .skills-content .left a:hover {
  color: rgb(231, 93, 0);
  background: none;
}

@media (max-width: 947px) {
  .max-width {
    max-width: 930px;
  }

  .skills .skills-content .column {
    width: 100%;
    margin-bottom: 0px;
  }
}

@media (max-width: 500px) {
  .skills .skills-content .left .text {
    font-size: 19px;
  }
  .about .title::after {
    font-size: 20px;
  }
}
</style>
