<template>
    <footer>
        <span>Created By <a href="#">Raveendra Hewage</a> | <span class="far fa-copyright"></span> 2021 All rights reserved.</span>
    </footer>
</template>

<script>
    export default {
        name:'Footer'
    }
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;700&family=Ubuntu:wght@400;500;700&display=swap');
footer{
    background: rgb(255, 255, 255);
    padding: 15px 23px;
    color: rgb(0, 0, 0);
    text-align: center;
    font-family: 'Poppins', sans-serif;
}
footer span a{
    color: rgb(231, 93, 0);
    text-decoration: none;
}
footer span a:hover{
    text-decoration: underline;
}
</style>