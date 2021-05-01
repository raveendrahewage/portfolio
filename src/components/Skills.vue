<template>
    <section class="skills" id="skills">
        <div class="max-width">
            <h2 class="title">My skills</h2>
            <div class="skills-content">
                <div class="column left">
                    <div class="text">My creative skills & experiences.</div>
                    <p>Since I am still a student, I don.t have much knowledge about many technologies and languages. But I am in the process of learning and getting more experiences.</p>
                    <div class="bars">
                        <div class="info">
                            <span>HTML</span>
                            <span>90%</span>
                        </div>
                        <div class="line html"></div>
                    </div>
                    <div class="bars">
                        <div class="info">
                            <span>CSS</span>
                            <span>40%</span>
                        </div>
                        <div class="line css"></div>
                    </div>
                    <div class="bars">
                        <div class="info">
                            <span>JavaScript</span>
                            <span>30%</span>
                        </div>
                        <div class="line js"></div>
                    </div>
                    <div class="bars">
                        <div class="info">
                            <span>PHP</span>
                            <span>40%</span>
                        </div>
                        <div class="line php"></div>
                    </div>
                </div>
                <div class="column right">
                    <!-- <div class="bars">
                        <div class="info">
                            <span>HTML</span>
                            <span>90%</span>
                        </div>
                        <div class="line html"></div>
                    </div>
                    <div class="bars">
                        <div class="info">
                            <span>CSS</span>
                            <span>40%</span>
                        </div>
                        <div class="line css"></div>
                    </div>
                    <div class="bars">
                        <div class="info">
                            <span>JavaScript</span>
                            <span>30%</span>
                        </div>
                        <div class="line js"></div>
                    </div>
                    <div class="bars">
                        <div class="info">
                            <span>PHP</span>
                            <span>40%</span>
                        </div>
                        <div class="line php"></div>
                    </div> -->
                    <div class="bars">
                        <div class="info">
                            <span>MySQL</span>
                            <span>60%</span>
                        </div>
                        <div class="line mysql"></div>
                    </div>
                    <div class="bars">
                        <div class="info">
                            <span>Vue.JS</span>
                            <span>30%</span>
                        </div>
                        <div class="line vue"></div>
                    </div>
                    <div class="bars">
                        <div class="info">
                            <span>C</span>
                            <span>50%</span>
                        </div>
                        <div class="line c"></div>
                    </div>
                    <div class="bars">
                        <div class="info">
                            <span>C++</span>
                            <span>40%</span>
                        </div>
                        <div class="line cplusplus"></div>
                    </div>
                    <div class="bars">
                        <div class="info">
                            <span>Java</span>
                            <span>35%</span>
                        </div>
                        <div class="line java"></div>
                    </div>
                    <div class="bars">
                        <div class="info">
                            <span>Pythons</span>
                            <span>20%</span>
                        </div>
                        <div class="line python"></div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
    export default {
        name:'Skills'
    }
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;700&family=Ubuntu:wght@400;500;700&display=swap');

*{
  box-sizing: border-box;
  text-decoration: none;
}

section{
    padding: 50px 0;
}

.max-width{
    max-width: 1300px;
    padding: 0 80px;
    margin: auto;
}

.skills{
    font-family: 'Poppins', sans-serif;
}

.skills .skills-content{
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    justify-content: space-between;
}

.title{
    position: relative;
    text-align: center;
    font-size: 40px;
    font-weight: 500;
    margin-bottom: 60px;
    padding-bottom: 20px;
    font-family: 'Ubuntu', sans-serif;
}

.title::before{
    content: "";
    position: absolute;
    bottom: 0px;
    left: 50%;
    width: 180px;
    height: 3px;
    background: #111;
    transform: translateX(-50%);
}

.title::after{
    position: absolute;
    bottom: -8px;
    left: 50%;
    font-size: 20px;
    color: rgb(231, 93, 0);
    padding: 0 5px;
    background: #fff;
    transform: translateX(-50%);
}

.skills .title::after{
    content: "what i know";
}

.skills .skills-content .column{
    width: calc(50% - 30px);
}

.skills .skills-content .left .text{
    font-size: 20px;
    font-weight: 600;
    margin-bottom: 10px;
}

.skills .skills-content .left p{
    text-align: justify;
}

.skills .skills-content .left a{
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

.skills .skills-content .left a:hover{
    color: rgb(231, 93, 0);
    background: none;
}

.skills .skills-content .right .bars{
    margin-bottom: 15px;
}

.skills .skills-content .left .bars{
    margin-bottom: 15px;
}

.skills .skills-content .right .info{
    display: flex;
    margin-bottom: 5px;
    align-items: center;
    justify-content: space-between;
}

.skills .skills-content .left .info{
    display: flex;
    margin-bottom: 5px;
    align-items: center;
    justify-content: space-between;
}

.skills .skills-content .right span{
    font-weight: 500;
    font-size: 18px;
}

.skills .skills-content .left span{
    font-weight: 500;
    font-size: 18px;
}

.skills .skills-content .right .line{
    height: 5px;
    width: 100%;
    background: lightgrey;
    position: relative;
}

.skills .skills-content .left .line{
    height: 5px;
    width: 100%;
    background: lightgrey;
    position: relative;
}

.skills .skills-content .right .line::before{
    content: "";
    position: absolute;
    height: 100%;
    left: 0;
    top: 0;
    background: rgb(231, 93, 0);
}

.skills .skills-content .left .line::before{
    content: "";
    position: absolute;
    height: 100%;
    left: 0;
    top: 0;
    background: rgb(231, 93, 0);
}

.skills-content .left .html::before{
    width: 90%;
}

.skills-content .left .css::before{
    width: 40%;
}

.skills-content .left .js::before{
    width: 30%;
}
.skills-content .left .php::before{
    width: 40%;
}

.skills-content .right .mysql::before{
    width: 60%;
}

.skills-content .right .vue::before{
    width: 30%;
}
.skills-content .right .c::before{
    width: 50%;
}
.skills-content .right .cplusplus::before{
    width: 40%;
}
.skills-content .right .java::before{
    width: 35%;
}
.skills-content .right .python::before{
    width: 20%;
}

@media (max-width: 947px){
    .max-width{
        max-width: 930px;
    }

    .skills .skills-content .column{
        width: 100%;
        margin-bottom: 0px;
    }
}

@media (max-width: 500px) {
    .skills .skills-content .left .text{
        font-size: 19px;
    }
}
</style>