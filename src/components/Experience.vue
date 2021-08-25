<template>
  <section class="experience" id="experience">
    <div class="max-width">
      <h2 class="title">Experience</h2>
      <div class="experience-content">
        <div class="column left">
          <img src="./../assets/promiseq.png" alt="" />
        </div>
        <div class="column right">
          <div class="text">
            <h3>promiseQ GmbH</h3>
            <br />
            <p>Gc/o The Drivery GmbH,</p>
            <p>Mariendorfer Damm 1,</p>
            <p>12099 Berlin.</p>
            <p>(2021 - Present)</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "experience",
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

section {
  padding: 50px 0;
}

.typing {
  color: rgb(231, 93, 0);
}

.experience {
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

.experience .experience-content {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  justify-content: space-between;
}

.experience .title::after {
  content: "where i was";
}
.experience .experience-content .left {
  width: 50%;
}
.experience .experience-content .left img {
  height: 400px;
  width: 400px;
  object-fit: cover;
  border-radius: 6px;
}
.experience .experience-content .right {
  width: 50%;
}
.experience .experience-content .right .text {
  margin-bottom: 10px;
}

.experience .experience-content .right .text h3 {
  font-size: 30px;
  margin: 0;
}

.experience .experience-content .right .text p {
  font-size: 25px;
  margin: 0;
}
.experience .experience-content .right .text :hover {
  color: rgb(231, 93, 0);
}
.experience .experience-content .right .text span {
  color: rgb(231, 93, 0);
}
.experience .experience-content .right p {
  text-align: justify;
}
.experience .experience-content .right a {
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
.experience .experience-content .right a:hover {
  color: rgb(231, 93, 0);
  background: none;
}

@media (max-width: 1104px) {
  .experience .experience-content .left img {
    height: 350px;
    width: 350px;
  }
}

@media (max-width: 947px) {
  .max-width {
    max-width: 930px;
  }
  .experience .experience-content .column {
    width: 100%;
  }
  .experience .experience-content .left {
    display: flex;
    justify-content: center;
    margin: 0 auto 60px;
  }
  .experience .experience-content .right {
    flex: 100%;
  }
}

@media (max-width: 500px) {
  .experience .experience-content .right .text {
    font-size: 19px;
  }
}
</style>
