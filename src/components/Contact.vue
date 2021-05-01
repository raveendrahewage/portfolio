<template>
    <section class="contact" id="contact">
        <div class="max-width">
            <h2 class="title">Contact me</h2>
            <div class="contact-content">
                <div class="column left">
                    <div class="text">Get in Touch</div>
                    <p>I am available on social media and you can contact me over them whenever you want. I will be there for you as quick as possible.</p>
                    <div class="icons">
                        <div class="row">
                            <i class="fas fa-user"></i>
                            <div class="info">
                                <div class="head">Name</div>
                                <div class="sub-title">Raveendra Hewage</div>
                            </div>
                        </div>
                        <div class="row">
                            <i class="fas fa-map-marker-alt"></i>
                            <div class="info">
                                <div class="head">Address</div>
                                <div class="sub-title">Singehraja Park, 10th Mile Post, Yattapatha</div>
                            </div>
                        </div>
                        <div class="row">
                            <i class="fas fa-envelope"></i>
                            <div class="info">
                                <div class="head">Email</div>
                                <div class="sub-title">hewagerv@gmail.com</div>
                            </div>
                        </div>
                        <div class="row">
                            <i class="fas fa-phone"></i>
                            <div class="info">
                                <div class="head">Phone</div>
                                <div class="sub-title">+94717188823</div>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="column right">
                    <div class="text">Social media</div>
                    <div class="contact-form">
                        <div class="field">
                            <a href="https://www.linkedin.com/in/raveendra-hewage-8763921b9/" class="fa fa-linkedin" target="_blank"><span>linkedin</span></a>
                        </div>
                        <div class="field">
                            <a href="https://www.facebook.com/ravindu.prashan.16/" class="fa fa-facebook" target="_blank"><span>facebook</span></a>
                        </div>
                        <div class="field">
                            <a href="https://twitter.com/HewageRaveendra" class="fa fa-twitter" target="_blank"><span>twitter</span></a>
                        </div>
                        <div class="field">
                            <a href="https://www.instagram.com/_rv__h/" class="fa fa-instagram" target="_blank"><span>instagram</span></a>
                        </div>
                        <div class="field">
                            <a href="https://github.com/raveendrahewage" class="fa fa-github" target="_blank"><span>github</span></a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
    export default {
        name:'Contact'
    }
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;700&family=Ubuntu:wght@400;500;700&display=swap');
@import url('https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css');

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

.contact{
    font-family: 'Poppins', sans-serif;
    color: white;
    background-color: black;
}

.contact .contact-content{
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
    background: rgb(255, 255, 255);
    transform: translateX(-50%);
}

.title::after{
    position: absolute;
    bottom: -8px;
    left: 50%;
    font-size: 20px;
    color: rgb(231, 93, 0);
    padding: 0 5px;
    background: rgb(0, 0, 0);
    transform: translateX(-50%);
}

.contact .title::after{
    content: "get in touch";
}

.contact .contact-content .column{
    width: calc(50% - 30px);
}

.contact .contact-content .text{
    font-size: 20px;
    font-weight: 600;
    margin-bottom: 10px;
}

.contact .contact-content .left p{
    text-align: justify;
}

.contact .contact-content .left .icons{
    margin: 10px 0;
}

.contact .contact-content .row{
    display: flex;
    height: 65px;
    align-items: center;
}

.contact .contact-content .row .info{
    margin-left: 30px;
}

.contact .contact-content .row i{
    font-size: 25px;
    color: rgb(231, 93, 0);
}

.contact .contact-content .info .head{
    font-weight: 500;
}

.contact .contact-content .info .sub-title{
    color: rgb(255, 255, 255);
}

.contact .right .contact-form .fields{
    display: flex;
}

.fa {
  padding: 20px;
  font-size: 30px;
  width: 42px;
  text-align: center;
  text-decoration: none;
  margin: 5px 2px;
}

.fa-facebook,.fa-twitter,.fa-linkedin,.fa-instagram ,.fa-github{
  color: rgb(231, 93, 0);
}

.contact .right .contact-form .field,
.contact .right .contact-form .fields .field{
    height: 45px;
    width: 100%;
    margin-bottom: 15px;
}

.contact .right .contact-form .field span{
    margin-left: 1rem;
    color: white;
    font-size: 25px;
}

.contact .right .contact-form .textarea{
    height: 80px;
    width: 100%;
}
.contact .right .contact-form .name{
    margin-right: 10px;
}

@media (max-width: 947px){
    .max-width{
        max-width: 930px;
    }

    .contact .contact-content .column{
        width: 100%;
        margin-bottom: 35px;
    }
}

@media (max-width: 500px) {
    .contact .right .contact-form .fields{
        flex-direction: column;
    }
    .contact .right .contact-form .name,
    .contact .right .contact-form .email{
        margin: 0;
    }
    .right .contact-form .error-box{
       width: 150px;
    }
}

</style>